Role ansible_galaxy_role.init
=========

This role will run plays that will make a system manageable by ansible.

Tasks:
- Create u_ansible user
- Set u_ansible user ssh keys
- Setup sudo to allow u_ansible user to run any command as root

The role should be called during bootstrapping when we can login to the remote system directly as root.
After that ansible should use u_ansible user to connect to the remote system.

Example Playbook
----------------
    - hosts: servers
      roles:
         - ansible_galaxy_role.init

To-Do: Use sudo module instead of file copy.