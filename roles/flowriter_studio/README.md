Role Name
=========

Deploys flowriter_studio

Requirements
------------

Root access

Role Variables
--------------

Defaults:
    # Deployment name for the app
    app_name: flowriter_studio
    # User which runs the app
    app_user: flowriter_studio
    # Port on which flowriter_studio runs
    app_port: 8000
    # Keyfile for flowriter_studio repo
    keyfile: id_rsa
    # Module that starts flask site
    flask_object_module: gen_time

Vars:
    # app_user's home directory
    app_user_home: /home/{{ app_user }}
    # Directory for app data
    app_dir: "{{ app_user_home}}/{{ app_name }}"
    # Directory for ssh keys
    ssh_dir: "{{ app_user_home}}/.ssh"
    # Destination for ssh keys
    keyfile_dest: "{{ ssh_dir }}/id_rsa"
    # systemd service file name
    service_file_name: "{{ app_name }}.service
    # systemd service file destination
    service_file_dest: /etc/systemd/system/{{ service_file_name }}

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: flowriter_studio, app_port: 8000 }

License
-------

GPLv3

Author Information
------------------

Jesse Bulson-Lewis, bulsonjg@whitman.edu
