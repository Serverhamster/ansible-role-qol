qol
=========

Alvin's personal Quality of Life improvements.

* [Powerline](https://powerline.readthedocs.io/en/latest/) (with vim and tmux support)
* [bat](https://github.com/sharkdp/bat) for man pages
* sudo without password
* [lsd](https://github.com/Peltoche/lsd) instead of ls
* alias for colorizing iproute2 tools

Requirements
------------

No special requirements

Role Variables
--------------

This role will only add the improvements for the **ansible_user**. If you want to make another user happy, set the **user** variable.

* **tmux**: boolean. Do you want tmux or not?
* **vim**: boolean. Do you want vim or not?

You can change the list of packages as well. See *defaults/main.yml*.


Example Playbook
----------------

```YAML
- hosts: localhost
  roles:
  - role: qol
```

Warnings
--------

* The `ll` command counts the total directory size. This can potentially take a long time
* `sudo` without password. Use at your own risk.
* You still need to have a font that contains powerline symbols.

License
-------

BSD

Author Information
------------------

This role was created in 2021 by Alvin Demeyer for himself.
