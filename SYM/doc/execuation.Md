ansible-playbook -i /etc/ansible/hosts /etc/ansible/playbooks/docker.yaml --limit "worker2"

ansible-playbook -i hosts playbooks/docker.yaml --extra-vars "target_group=worker2"
ansible-playbook -i hosts playbooks/docker.yaml --extra-vars "target_group=172.31.34.181"



ansible-playbook -i inventory/inventory.ini playbooks/sap-hana-status.yml -u symadm
ansible-playbook -i inventory/inventory.ini playbooks/sap-hana-status.yml

ansible-playbook -i hosts playbooks/docker.yaml --extra-vars "target_group=worker1,worker2"

ansible-playbook -i hosts playbooks/docker.yaml --extra-vars "target_group=172.31.34.181,172.31.34.182"
