# apt-repository

Role for handling apt repositories.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Notes
-----
This role is meant to be depended on for other roles, to reduce boilerplate code in playbooks.

Tunables
--------
* repository_url (string): URL to add to sources.list
* repository_key (string): ID for repository signing key. This will be imported into the apt keychain.

Dependencies
------------
* None

Example Usage
-------------
    ---
    dependencies:
      - role: telusdigital.apt-repository
        repository_key: "0x0000000000000000"
        repository_url: "deb http://ppa.launchpad.net/SOME_REPOSITORY {{ ansible_distribution_release }} main"

License
-------
[MIT](https://tldrlegal.com/license/mit-license)

Contributors
------------
* [Chris Olstrom](https://colstrom.github.io/) | [e-mail](mailto:chris@olstrom.com) | [Twitter](https://twitter.com/ChrisOlstrom)
