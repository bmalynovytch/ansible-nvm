This Ansible role is a rework of [leonidas' ansible-nvm](https://github.com/leonidas/ansible-nvm), with compatibility with Ansible 2.0+

nvm
========

Install nvm and Node.js.

Requirements
------------

git, curl, build-essential, libssl-dev. Requirements are installed by the role.

Role Variables
--------------

* `nvm.user` Remote user. Defaults to ansible `remote_user`.
* `nvm.version` nvm version tag, or `HEAD`. Defaults to `v0.31.0`
* `nvm.node_version` Node.js version. Defaults to `'v4.4.3'`

Dependencies
------------

No depedencies.

Example Playbook
-------------------------

    - hosts: servers
      roles:
        - role: nvm
          nvm:
            user: node
            version: v0.31.0
            node_version: v4.4.3

