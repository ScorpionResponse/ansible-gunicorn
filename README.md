Ansible Role: gunicorn
======================

[![Build Status](https://travis-ci.org/ScorpionResponse/ansible-gunicorn.svg?branch=master)](https://travis-ci.org/ScorpionResponse/ansible-gunicorn)

Ansible role to install gunicorn.

Requirements
------------

None.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

* The ScorpionResponse.pip role will be used to install pip
* The ScorpionResponse.supervisord role will be use to install supervisord and
  run gunicorn with that.

Example Playbook
----------------

Example usage:

    - hosts: all
      roles:
         - { role: ScorpionResponse.gunicorn }

License
-------

BSD

Author Information
------------------

Github: https://github.com/ScorpionResponse
