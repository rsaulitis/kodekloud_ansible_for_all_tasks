# For use on jump host when you whant to complete task with ansible not manually on each desired host
Install git

    sudo yum install -y git

Clone this repo

    git clone https://github.com/rsaulitis/kodekloud_ansible_for_all_tasks.git

CD to got folder
Run setup script

    sudo sh ./setup.sh

Do not edit first 5 lines in playbook. Edit playbook for your task needs and run playbook:

    ansible-playbook playbook.yml --extra-vars "host=(hostname or host group from inventory) other_variable=foo"

For example:

    ansible-playbook playbook.yml --extra-vars "host=stapp01 username=JohnDoe"
