# ERASME Ansible Playbooks Collection

ERASME       @erasme
Michel Blanc @leucos

# rbenv playbook

This playbook will install rbenv in a user's home directory.
You can then leverage rbenv to install rubies for this user.

# Variables

  - `ruby_deploy_user`: taget user for rbenv installation; required; no
    default
  - `rbenv_makeopts`: Make options when building a ruby version;
    optional; default: -j2

# Tags

  - rbenv
  - ruby
  - ruby:install

# Notes

This role goes along with the ruby role. Check the latter to see usage
information.

# Licence

MIT

