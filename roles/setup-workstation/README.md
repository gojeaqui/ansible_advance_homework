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

Example Playbook
----------------

    - hosts: workstation
      roles:
         - setup-workstation

