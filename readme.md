# For use on jump host when you whant to complete task with ansible not manually on each desired host

1. Install git

    echo "mjolnir123" | sudo -S -k yum install -y git

2. Clone this repo

    git clone <https://github.com/rsaulitis/kodekloud_ansible_for_all_tasks.git>

3. CD to cloned git folder
4. Run setup script

    sudo sh ./setup.sh

5. Edit playbook for your task needs and run playbook. Do not edit first 5 lines in playbook:

    ansible-playbook playbook.yml --extra-vars "host=(hostname or host group from inventory) other_variable=foo"

For example:

    ansible-playbook playbook.yml --extra-vars "host=stapp01 username=JohnDoe"

Full example:

    echo "mjolnir123" | sudo -S -k yum install -y git
    git clone https://github.com/rsaulitis/kodekloud_ansible_for_all_tasks.git
    cd kodekloud_ansible_for_all_tasks
    sudo sh ./setup.sh
    ansible-playbook playbook.yml --extra-vars "host=stapp01 username=JohnDoe"
