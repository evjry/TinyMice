# Welcome!
Hello to my repository, this is TinyMice distribution made by me to you. Project is not ready but you can see progress here.

# Description
TinyMice is a linux distribution created from scratch (lfs), which uses BusyBox as temporary bootstrapping foundation while i slowly rewrite **every** command in C.

The goal of this project is to create a lightweight, easy to use and most importantly from scratch.
The best i want to leave as premade is kernel.

# Project status:
Progress: 10/200+ commands; graphics: 1/100%;
Current core: Linux Kernel + BusyBox

# Completed:
* rm;
* rmdir;
* mkdir;
* pwd;
* cd;
* kill;
* echo;
* power;
* touch;
* cp;

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

## Section 3: Building TinyMice
1. Run Makefile using `make run`

## Section 4: Explanation
1. Makefile downloads/clones the kernel and copies the backed-up config into the linux directory;
2. Makefile compiles the custom shell and commands by using GCC;
3. Makefile packages shell and custom commands into an initramfs archive named init.cpio using cpio command;
4. Makefile builds the kernel image;
5. Makefile creates virtual disk (.img file) using qemu-img;
6. Makefile mounts image and installs grub;
7. Makefile runs the generated bootable .iso file inside qemu

# Tree
```text
.
├── config/ (linux kernel config file backup)
├── internal/
│   ├── linux/ (kernel)
│   ├── shell/
│   │   ├── mice.c
│   ├── graphics/
├── rootfs/
│   ├── compiled commands and init
├── src/
│   ├── source code of commands
├── assets/
│   ├── disk file
├── mnt/ (mount directory)
└──
```
