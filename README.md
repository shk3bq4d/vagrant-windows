ansible-playbook -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory windows.yml
vagrant up
.vagrant up --provision
vagrant destroy -f; sleep 10; vagrant up
