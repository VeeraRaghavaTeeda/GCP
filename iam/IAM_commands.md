#updating the iam roles 
$>gcloud iam roles describe projects/testing-387105/roles/CustomRole --project=testing-387105

output:

description: 'Created on: 2023-05-19'
etag: BwX8DqGXG9k=
includedPermissions:
- compute.disks.create
- compute.instances.attachDisk
- compute.instances.create
- compute.instances.delete
- compute.instances.setMetadata
- compute.instances.setServiceAccount
- compute.instances.start
- compute.instances.stop
- compute.instances.suspend
- compute.subnetworks.use
- compute.subnetworks.useExternalIp
name: projects/testing-387105/roles/CustomRole
stage: ALPHA
title: Testing-Custom-role
now update the role for above the out and save the file with roleupdate.yaml

$>gcloud iam roles update CustomRole --project=testing-387105 --file=roleupdate.yaml


