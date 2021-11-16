# Create Jenkins instance on GCP
1. copy "create-jenkin-vm" to project
2. change following configuration to your project
```
gcp_project: [put your gcp project id]
gcp_cred_file: [path of your service account json]
```
3. run the ansible command to execute
```
$> ansible-playbook create-jenkin-vm
```
