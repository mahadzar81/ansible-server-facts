# ansible-server-facts
Ansible export server facts to simple csv file. You can get more information on ansible server facts from [Ansible facts]
This playbook inspired by [Ansible export facts to simple csv file]. This works with ansible core version 2.14.5

## Description
This script does following:

"*" Generate CSV filename using date
"*" Put in a header int the output file
"*" Get facts from remote server and write it to a temporary file called csv_tmp
"*" Write data into the final export file in controller node
"*" Remove blank lines from csv

## Usage
```
ansible-playbook -u <user> --private-key ~/.ssh/id_rsa -i <inventory files> gathering_server_facts_playbook.yml
```

[Ansible facts]: https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_vars_facts.html
[Ansible export facts to simple csv file]: https://www.uni-koeln.de/~pbogusze/posts/Ansible_export_facts_to_simple_csv_file.html
