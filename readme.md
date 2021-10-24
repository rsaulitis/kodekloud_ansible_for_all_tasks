# For use on jump host when you whant to complete task with ansible not manually on each desired host

1. Install git:

    echo "mjolnir123" | sudo -S -k yum install -y git
  
2. Install ansible:

    echo "mjolnir123" | sudo -S -k yum install -y ansible

3. Clone this repo:

    git clone <https://github.com/rsaulitis/kodekloud_ansible_for_all_tasks.git>

4. CD to cloned git folder

5. Edit playbook for your task needs and run playbook. Host or Hosts on which to run tasks need to be parsed in command line or edited in playbook:

    ansible-playbook playbook.yml --extra-vars "host=(hostname or host group from inventory) other_variable=foo"

For example:

    ansible-playbook playbook.yml --extra-vars "host=stapp01 username=JohnDoe"

Full example:

    echo "mjolnir123" | sudo -S -k yum install -y git
    echo "mjolnir123" | sudo -S -k yum install -y ansible
    git clone https://github.com/rsaulitis/kodekloud_ansible_for_all_tasks.git
    cd kodekloud_ansible_for_all_tasks
    ansible-playbook playbook.yml --extra-vars "host=stapp01 username=JohnDoe"
