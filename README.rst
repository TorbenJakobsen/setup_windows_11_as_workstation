###################################
  Setup Windows 11 as Workstation
###################################

Introduction
------------

Documents my personal setup.

A better way is to use (alternative PS) Ansible, and I will get there eventually.

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

The general guide is here:
https://code.visualstudio.com/docs/setup/linux

Install :code:`code` Extensions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can use the command line to list and install/uninstall extensions.

Examples:

.. code:: bash 

  code --list-extensions
  code --install-extension redhat.vscode-yaml
  code --uninstall-extension timonwong.shellcheck

My personal preferences are:

| :code:`ms-python.python`
| :code:`ms-python.vscode-pylance`

.. code:: text

  aaron-bond.better-comments
  davidanson.vscode-markdownlint
  docker.docker
  donjayamanne.python-environment-manager
  dracula-theme.theme-dracula
  github.codespaces
  github.vscode-github-actions
  ibm.ibm-developer
  ibmconsulting.ica
  inferrinizzard.prettier-sql-vscode
  jakebecker.elixir-ls
  lextudio.iis
  lextudio.restructuredtext-pack
  mechatroner.rainbow-csv
  ms-azuretools.vscode-docker
  ms-python.black-formatter
  ms-python.debugpy
  ms-python.isort
  ms-python.python
  ms-python.vscode-pylance
  ms-toolsai.jupyter
  ms-toolsai.jupyter-keymap
  ms-toolsai.jupyter-renderers
  ms-toolsai.vscode-jupyter-cell-tags
  ms-toolsai.vscode-jupyter-slideshow
  ms-vscode-remote.remote-containers
  ms-vscode-remote.remote-ssh
  ms-vscode-remote.remote-ssh-edit
  ms-vscode.makefile-tools
  ms-vscode.remote-explorer
  njpwerner.autodocstring
  quarto.quarto
  redhat.ansible
  redhat.vscode-yaml
  sapos.yeoman-ui
  saposs.app-studio-remote-access
  saposs.app-studio-toolkit
  saposs.sap-guided-answers-extension
  saposs.vscode-ui5-language-assistant
  saposs.xml-toolkit
  sapse.sap-ux-annotation-modeler-extension
  sapse.sap-ux-application-modeler-extension
  sapse.sap-ux-fiori-tools-extension-pack
  sapse.sap-ux-help-extension
  sapse.sap-ux-service-modeler-extension
  shuworks.vscode-table-formatter
  sonarsource.sonarlint-vscode
  swyddfa.esbonio
  tamasfe.even-better-toml
  trond-snekvik.simple-rst
  wesbos.theme-cobalt2
  wholroyd.jinja

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

