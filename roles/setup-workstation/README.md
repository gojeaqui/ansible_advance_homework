setup-workstation
=================

This role sets up the workstation

Tasks
-----

 * main.yml
   * Main playbook, include_tasks: the other playbooks in order

 * pre-tasks.yml
   * Installs openstacksdk library
   * Creates clouds.yaml file
   * Sets openstack.pub authorized key from file

 * create-flavor.yml
   * Creates m2.small flavor

 * create-keypair.yml
   * Generates key files
   * Creates OSP keypair

 * create-sg.yml
   * Creates Security Group Apps
   * Creates Security Group Rule Apps
   * Creates Security Group Frontend
   * Creates Security Group Rule Frontend
   * Creates Security Group DB
   * Creates Security Group Rule DB

 * create-image.yml
   * Downloads RHEL image
   * Creates openstack image

 * create-network.yml
   * Configures Public and Private Networks on OSP
   * Configures Subnets for Public and Private SubNets
   * Creates Router

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: workstation
      roles:
         - { role: setup-workstation, x: 42 }

