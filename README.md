Ansible Examples 
----------------

```
# Populate the local hosts file with the IP address(s) AWS servers created with and 'Ansible' Key tag
aws ec2 describe-instances --filters "Name=tag-key,Values=Ansible" | grep PublicIpAddress | awk -F ":" '{print $2}' | sed 's/[",]//g' > hosts

```
