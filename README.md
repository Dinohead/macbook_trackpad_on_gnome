# macbook_trackpad_on_gnome

This is a role that configures the mtrack trackpad module for MacBooks. This was adapted from the guide found here: https://howchoo.com/g/mdy0ngziogm/the-perfect-almost-touchpad-settings-on-linux-2

## Requirements

I have only tested this on a Macbook Pro mid 2010 running Centos 7.

* Gnome
* Xorg
* Yum

## Role Variables

All variables used in this role are defined using a <code>macbook_trackpad_on_gnome</code> dictionary. The dictionary is defined in macbook_trackpad_on_gnome/defaults/main.yml. This dictionary can be overriden when called or in any standard "ansible" way. 


### Options:

|parameter|required|default|choices|comments|
|---|---|---|---|---|
|install_dir|true|~/macbook_trackpad_on_gnome_install| |This is the temporary directory the role will use for staging files|


## Example Playbook

###### Apply role and accept defaults
```yaml
- name: PLAY | Apply install_ohs role
  hosts: [centos-workstation]
  roles:
  - role: macbook_trackpad_on_gnome
```

###### Apply role and change the temporary install directory
```yaml
- name: PLAY | Apply macbook_trackpad_on_gnome role
  hosts: [centos-workstation]
  roles: 
  - role: macbook_trackpad_on_gnome
    macbook_trackpad_on_gnome:
        install_dir: '/u01'    
```

## License

TBD

## Author Information

|Author|E-mail|
|---|---|
|Derek 'dRock' Halsey|derek@dinohead.io|

## Role Development Information

### Git SCM
Please refer to the .gitignore file and update accordingly depending on your
development environment, etc.  The particular file was generated at 
gitignore.io and contains settings for the following:
  - Ansible
  - Python
  - Vim
  - Eclipse
  - IntelliJ IDEA
  - Linux
  - Windows
  
### Versioning
Please update VERSION.md as you release new versions of your role and try to
abide by Semantic Versioning (compatibility).

Please consider using Gitflow such that individuals that want to use your role
can identify a version (e.g. master, develop, <tag>, etc.) to use.
  - https://danielkummer.github.io/git-flow-cheatsheet/
  - http://nvie.com/posts/a-successful-git-branching-model/

### Self-contained
Please try to keep this role as self-contained as possible such that it may be
simply installed (e.g. ansible-galaxy install) and applied as part of a 
playbook.