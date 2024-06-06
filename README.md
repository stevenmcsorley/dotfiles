# Dotfiles

This repository contains my personal configuration files (dotfiles) for various tools and applications. It uses [GNU Stow](https://www.gnu.org/software/stow/) to manage symlinks, making it easy to keep everything organized and portable.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Scripts](#scripts)
  - [Neovim](#neovim)
- [Directory Structure](#directory-structure)

## Installation

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/stevenmcsorley/dotfiles.git ~/dotfiles
    ```

2. **Install GNU Stow**:
    If you don't have GNU Stow installed, you can install it using your package manager. For example, on Debian-based systems:
    ```sh
    sudo apt-get install stow
    ```
Or use this Ansible script to install the version with the directory bug fix here:
    ```sh
    git clone https://github.com/stevenmcsorley/ansiblesetups ~/ansible_setups
    ```

## Usage

### Scripts

To manage your custom scripts and add them to your `~/bin` directory, use the following command:

```sh
stow --target=$HOME/bin bin
```

This will create symlinks for all scripts in the `bin` directory of this repository to your `~/bin` directory.

### Neovim

To manage your Neovim configuration and add it to your `~/.config/nvim` directory, use the following command:

```sh
stow --target=$HOME/.config/nvim nvim
```
This will create symlinks for all Neovim configuration files in the `nvim` directory of this repository to your `~/.config/nvim` directory.

### Directory Structure

The repository is organized as follows:

dotfiles
├── bin
│ └── tmux-sessionizer
└── nvim
└── init.lua


- **bin**: Contains custom scripts that you want to add to your `~/bin` directory.
- **nvim**: Contains Neovim configuration files that you want to add to your `~/.config/nvim` directory.

