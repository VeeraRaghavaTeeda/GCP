# tologin to gcloud from sdk
gcloud auth login

# Setting up the project
gcloud config set project <project ID>
gcloud config set project testing-387105

# to see the config list of current project  
gcloud config list

# to set the project to particular region 
gcloud config set compute/region us-central1

#to set the project to particular zone
gcloud config set compute/zone us-central1-a


# to get auth details 
gcloud auth list

# to get the list project under that user 
gcloud projects list

# to switch from one project to another 
 gcloud config set project <project ID>
 
# to set the zone or region 
gcloud config unset compute/zone
gcloud config unset compute/region 
 