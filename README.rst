###################################
  Setup Windows 11 as Workstation
###################################

************
  Preamble
************

The preamble is mostly universal for the repositories linked herein.

This is part of multiple notes about my *personal* setup of various Linux and BSD distributions. 
Some are used as desktops or servers or as virtual machines and containers. 
Each has a flavour and tweaks I will document in these lab notes.

- `Setup CentOS Linux as Server <https://github.com/TorbenJakobsen/setup_centos_linux_as_server/>`__
- `Setup Debian Linux as Server <https://github.com/TorbenJakobsen/setup_debian_linux_as_server/>`__
- `Setup Debian Linux as Workstation <https://github.com/TorbenJakobsen/setup_debian_linux_as_workstation/>`__
- `Setup Fedora Linux as Workstation <https://github.com/TorbenJakobsen/setup_fedora_linux_as_workstation/>`__
- `Setup FreeBSD as Workstationm <https://github.com/TorbenJakobsen/setup_freebsd_as_workstation/>`__
- `Setup macOS as Workstation <https://github.com/TorbenJakobsen/setup_macos_as_workstation/>`__
- `Setup Proxmox as Hypervisor <https://github.com/TorbenJakobsen/setup_proxmox_as_hypervisor/>`__
- `Setup Windows 11 as Workstation <https://github.com/TorbenJakobsen/setup_windows_11_as_workstation/>`__

Additionally there some common components and setup.

- `Manage configuration with GNU stow <https://github.com/TorbenJakobsen/manage_configuration_with_stow/>`__ 
- `Setup Python for Development <https://github.com/TorbenJakobsen/setup_python_for_development/>`__ 
- `Setup Terminal and Shell <https://github.com/TorbenJakobsen/setup_terminal_and_shell/>`__ 
- `Setup Visual Studio Code <https://github.com/TorbenJakobsen/setup_visual_studio_code/>`__ 

I also have a crude utility to syncronize and 
`manage GitHub repositories <https://github.com/TorbenJakobsen/manage_github_repos/>`__
with these notes sufficient for my personal needs.

We are all different with different knowledge and foundation,
so I appologize in advance if steps are missing or skipped.

****************
  Introduction
****************

A definite better way than manual steps
is to use (alternative PS) Ansible_  (or similar),
and I will get there eventually.

Initial Housekeeping
--------------------

Package manager
~~~~~~~~~~~~~~~~

Initial update
~~~~~~~~~~~~~~

.. note:: 

  Make sure you have a network connection.

After the build of the installation media many changes will likely
have been added to your system.
So a full update is in place.

You can check available update packages beforehand:

Depending on your updates you should restart the system.
Strictly you could probaly get away with restarting some sub-systems,
but it will likely be faster just restarting instead of micro-managing services and daemons.

Install prefered Terminal and Shell
===================================

This topic has its own page:
https://github.com/TorbenJakobsen/setup_terminal_and_shell.


install :code:`ansible`
-----------------------

https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html

install the full package:

.. code:: bash

  ...

It is also possible to install just the core and modules of your choosing.

Install WSL2
------------

:code:`ssh`` Keys
-----------------

To access :ode:`git` you will need a public key.

Install :code:`gìt`
-------------------

.. code:: bash

  ...

Follow:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

.. code:: bash

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
  git config --global init.defaultBranch "main"

Depending on your preferences. 
Personally I like :code:`code` to open. You may prefer :code:`vim` or the default.

.. code:: bash

  git config --global core.editor "code --wait"

Optionally install public key in GitHub
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I use GitHub and other services and have other servers that I want to access.

To install public key in GitHub follow ...

Install Visual Studio Code
--------------------------

The official guide is
`here <https://code.visualstudio.com/docs/setup/windows>`__.

Finalize installation by following 
`Setup Visual Studio Code <https://github.com/TorbenJakobsen/setup_visual_studio_code/>`__.

Install Docker
--------------

The general installation:
https://docs.docker.com/engine/install/

Docker Desktop and podman???

Setup `zsh` as default shell
----------------------------

Configure omz

Configure shell prompt

Other packages to consider
--------------------------

GPU drivers:
https://www.nvidia.com/en-us/drivers/
