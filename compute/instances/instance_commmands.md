#creating virtual machines 
gcloud compute instances create devlopment-01 --project=manifest-wind-376615 --zone=us-central1-a --machine-type=e2-medium




# creating the vm using the instance-groups
gcloud beta compute instance-groups managed create dev-env --project=manifest-wind-376615 --base-instance-name=dev-env --size=1 --template=fresh-template --zone=us-central1-a  --health-check=health --initial-delay=300 




##seting autscaling for instanc group 
gcloud beta compute instance-groups managed set-autoscaling dev-env --project=manifest-wind-376615 --zone=us-central1-a --cool-down-period=60 --max-num-replicas=3 --min-num-replicas=1 --mode=on --target-cpu-utilization=0.6