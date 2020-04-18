## **Useful Commands**

* ansible-playbook deploy.yml -K -vvvv -i <hostfile> --tags=<tags> --limit=<limit>
* ansible-playbook deploy.yml -K -vvvv -i <hostfile> --tags=<tags> --limit=<limit> --list-hosts
* ansible-playbook deploy.yml -K -vvvv -i <hostfile> --tags=<tags> --limit=<limit> --list-tasks


#Document to follow after deployment
https://work.greyorange.com/confluence/display/LSS/SAPP+HUL+Configuration+Setup

##Sample Command with username, password argument for changing password

*  ansible-playbook deploy.yml -K -vvvv -i clients/rpc/staging --tags=changePassword --extra-vars='{"username": "username", "password": "password"}'

##Sample Command with installation_type argument for creating configuration
* ansible-playbook deploy.yml -K -vvvv -i clients/rpc/staging --tags=setup --extra-vars='{"installation_type": 1}'