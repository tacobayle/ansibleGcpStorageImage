# aviGcp

## Goals
Prepare GCP before deploying Avi controller

## Prerequisites:
- Ansible in the orchestrator VM
- gdown in the orchestrator VM (pip install gdown)

## Environment:

Playbook(s) has/have been tested against:

### ansible

```
ubuntu@jump:~$ ansible --version
ansible 2.9.12
  config file = None
  configured module search path = [u'/home/ubuntu/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python2.7/dist-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 2.7.17 (default, Jul 20 2020, 15:37:01) [GCC 7.5.0]
ubuntu@jump:~$
```


## Input/Parameters:

The following parameters are required:
- googleDriveId # where to download Avi
- buckeAvi # name of the bucket
- googleProject # gcp project name
- googleEmail # gcp email cred


## Use the the ansible playbooks to:
1. Download Avi files to the jump server (from Google Drive)
2. Create a GCP storage bucket
3. Download the Avi image to the jump server (via Ansible)
4. Upload the Avi image to the bucket (via Ansible)
5. Create an GCP image (via Ansible)

## Run the ansible playbook:
```
ansible-playbook local.yml
```
