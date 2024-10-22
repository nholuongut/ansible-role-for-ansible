# Ansible Role: Ansible

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

An Ansible Role that installs Ansible on Linux servers.

## Requirements

If using on a RedHat/CentOS/Rocky Linux-based host, make sure you've added the EPEL repository (it can easily be installed by including the `nholuong.repo-epel` role on Ansible Galaxy).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ansible_install_method: package

Whether to install Ansible via the system `package` manager (`apt`, `yum`, `dnf`, etc.), or via `pip`. If set to `pip`, you need to make sure Pip is installed prior to running this role. You can use the `nholuong.pip` module to install Pip easily.

    ansible_install_version_pip: ''

If `ansible_install_method` is set to `pip`, the specific Ansible version to be installed via Pip. If not set, the latest version of Ansible will be installed.

## Dependencies

None.

## Example Playbook

Install from the system package manager:

    - hosts: servers
      roles:
        - role: nholuong.ansible

Install from pip:

    - hosts: servers
      vars:
        ansible_install_method: pip
        ansible_install_version_pip: "2.7.0"
      roles:
        - role: nholuong.pip
        - role: nholuong.ansible

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
