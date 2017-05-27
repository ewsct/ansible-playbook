# Vim role

This role installs and configures Vim.

> Your current vim configuration will be removed.

You may skip some options with adding extra-vars. Supported options:
- install
- icons
- nerdtree
- powerline
- pathogen
- install\_themes
- golang

Set the option you want to skip to False or No, e.g. `--extra-vars "install=False"`

You may choose a theme that will be set. Supported themes:
- seti
- mirodark

To choose a theme simply add `--extra-vars "theme=<theme_name>"`
