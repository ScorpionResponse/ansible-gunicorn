Ansible Role: gunicorn
======================

[![Build Status](https://travis-ci.org/ScorpionResponse/ansible-gunicorn.svg?branch=master)](https://travis-ci.org/ScorpionResponse/ansible-gunicorn)

Ansible role to install gunicorn.

Requirements
------------

None.

Role Variables
--------------

### Required
* `gunicorn_project_dir`: The directory of the project containing the wsgi
  application.  Example: /var/www/django_app
* `gunicorn_wsgi_application`: The wsgi application to invoke.  Example:
  myapp.wsgi:application

### Optional
* `gunicorn_bind_address`: The bind method for communication with gunicorn.
  Default: unix:/var/run/gunicorn.sock
* `gunicorn_log_level`: The logging level.  Default: info
* `gunicorn_config_dir`: The directory to be used for config info.  Default:
  /etc/gunicorn
* `gunicorn_log_dir`: The directory to store logs.  Default: /var/log/gunicorn
* `gunicorn_user_name`: The user account to run gunicorn under. Default:
  gunicorn
* `gunicorn_group_name`: The group to run gunicorn under. Default: gunicorn
* `gunicorn_install_path`: The folder containing the gunicorn executable.
  Change if you're using a virtualenv version of this.
* `gunicorn_reload`: Whether to activate hot-reloading of code (for
  development).  Default: false
* `gunicorn_workers`: The number of workers to instantiate. Default: 8

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
