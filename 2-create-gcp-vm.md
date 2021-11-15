# Create VM instance on GCP
1. copy "create-vm" to project
2. change following configuration to your project
```
gcp_project: [put your gcp project id]
gcp_cred_file: [path of your service account json]
```
3. run the ansible command to execute
```
$> ansible-playbook create-vm
```

# Find google image list
1. for gcp_compute_disk.source_image can find with the following command
```
$> gcloud compute images list --uri
```

# Clear authenticated ssh once create instance
Once you create GCP instance with ansible,
ansible may automatically create ssh from your local machine to created GCP instance.
So if you run this script twice then get the same IP from GCP, the ssh may not work.
1. to fix this problem kindly delete the row the contain GCP IP on ~/.ssh/known_hosts
