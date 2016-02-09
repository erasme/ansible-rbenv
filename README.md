rbenv Ansible playbook
======================

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-rbenv.svg?style=flat)](http://travis-ci.org/erasme/ansible-ruby)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--rbenv-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-rbenv/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.rbenv-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2909)

This playbook will install rbenv in a user's home directory.
You can then leverage rbenv to install rubies for this user.

Requirements
------------

None

Role Variables
--------------

  - `ruby_deploy_user`: target user for rbenv installation; required; no
    default
  - `rbenv_makeopts`: Make options when building a ruby version;
    optional; default: -j2

Tags
----

  - rbenv
  - ruby
  - ruby:install

Dependencies
------------

  - erasme.ruby-compiled

Example Playbook
----------------

This is mainly used as a dependency in combination with the
[erasme.ruby](https://galaxy.ansible.com/list#/roles/2925) role, like :

    dependencies:
      - { role: erasme.rbenv }
      - { role: erasme.ruby-compiled,
          ruby_version: "2.2.0" }

Note however that erasme.rbenv is automatically listed as a dependency in the
erasme.ruby role, so it shouldn't be necessary to add it explicitely to your
projects.

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

