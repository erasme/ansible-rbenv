rbenv
=====

This playbook will install rbenv in a user's home directory.
You can then leverage rbenv to install rubies for this user.

Requirements
------------

None

Role Variables
--------------

  - `ruby_deploy_user`: taget user for rbenv installation; required; no
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

  - erasme.ruby

Example Playbook
----------------

This is mainly used as a dependency in combination with the erasme.ruby role, like :

    dependencies:
      - { role: rbenv }
      - { role: ruby,
          version: "2.2.0",
          ruby_default: "2.2.0" }

Note however that rbenv is automatically listed as a dependency in the erasme.ruby role, so it shouldn't be necessary to add it explicitely to your projects.

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

