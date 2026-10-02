# Welcome!
Hello to my repository, this is TinyMice distribution made by me to you.

# Description
TinyMice is a linux distribution created from scratch (lfs), which uses BusyBox as temporary bootstrapping foundation while i slowly rewrite **every** command in C.

The goal of this project is to create a lightweight, easy to use and most importantly from scratch.
The best i want to leave as premade is kernel.

# Project status:
Progress: 4/200+ commands;
Current core: Linux Kernel + BusyBox

# Completed:
* rm;
* rmdir;
* pwd;
* cd

# Commands that i am currently making that isn't put by default:
* ers (EasyResourceMonitor);

# How To Build (HTB)
Required:
* build-essential;
* libncurses-dev;
* libssl-dev and libelf-dev;
* bison and flex;
* bc;
* git;
* qemu (or any other emulator to run the TinyMice image.)

## Section 1: Installing dependencies
1. Use `sudo apt install build-essential libncurses-dev libssl-dev libelf-dev bison flex bc git qemu-system-x86`

## Section 2: Cloning the repository
1. Use `git clone https://github.com/evjry/TinyMice && cd TinyMice`

## Section 2: Building TinyMice
1. Run Makefile using `make`

# Tree
.
├── cmd (commands)
├── config (linux kernel config file backup)
├── shell (shell file)
├── tinymice_root (root commands directory)
│   ├── bin
│   ├── dev
│   ├── etc
│   ├── proc
│   ├── sbin
│   ├── sys
│   └── usr
│       ├── bin
│       └── sbin
└── tinymouse (my own desktop environment)
    ├── include
    └── src


