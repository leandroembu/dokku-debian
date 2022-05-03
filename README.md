Dokku Debian
===

> A simple role to install Dokku on Debian servers.

Requirements
------------

- A working Debian sever with ssh access
- A user with sudo privileges
- A local machine with ansible installed

How to run this role
------------

- Create a folder with playbook.yml and inventory files
- In this folder, clone this repo
- Run the playbook (see the example playbook in the next section):
`ansible-playbook -i inventory playbook.yml --become -K`

Project tree:
```
your-project-folder
├── dokku-debian (this repo)
│   ├── defaults
│   │   └── main.yml
│   ├── handlers
│   │   └── main.yml
│   ├── LICENSE
│   ├── meta
│   │   └── main.yml
│   ├── README.md
│   ├── tasks
│   │   └── main.yml
│   ├── tests
│   │   ├── inventory
│   │   └── test.yml
│   └── vars
│       └── main.yml
├── inventory
└── playbook.yml
```

Example Playbook
----------------

```
- hosts: all
  roles:
    - { role: dokku-debian, become: yes }
```

License
-------

GNU GPL v3.0

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
