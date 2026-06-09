# Cloud-Infrastructure-Projects
Overview
This repository contains two hands-on technical projects covering Linux server administration, virtualisation and container technologies. Both projects were executed entirely through the command line with absolutely no graphical interface at any point. The goal was to build real, production-style infrastructure from scratch and understand every layer of the stack — from bare disk to running containers.

 Projects
 
1. Baremetal-Arch-Linux-Server-Configuration.pdf
A complete Linux server was built from a blank virtual disk using VMware Workstation Pro. The entire process was carried out through the terminal only — no installation wizard, no GUI, no shortcuts.
What was covered:

Created a 40GB virtual disk and partitioned it using GPT partition table with separate EFI, home and root partitions using cfdisk
Formatted partitions with FAT32 and EXT4 filesystems and mounted them correctly
Refreshed the pacman keyring to resolve PGP signature errors before installation
Installed the Arch Linux base system manually using pacstrap
Configured timezone (Asia/Kathmandu), locale, hostname and hosts file inside chroot
Installed and enabled NetworkManager and GRUB bootloader
Set strong root password and disabled direct root SSH login
Restricted su access to wheel group members only via PAM configuration
Created two admin accounts with full sudo access via wheel group
Created role-based user accounts for developers, web developers and testers
Applied setgid bit on shared directories so new files automatically inherit group ownership
Configured POSIX ACLs for fine-grained permission control across multiple groups
Restricted one user to SFTP-only access inside a chroot jail using OpenSSH Match block
Configured SSH whitelist, disabled X11 forwarding and limited brute-force attempts
Deployed a full Docker stack with three containers — Nginx, MySQL and PhpMyAdmin
Configured Nginx as a reverse proxy — database never exposed to the outside world
Granted database administrator privileges inside the MySQL container


2. Docker-Container-Lifecycle-Management.pdf
A structured hands-on project covering the full lifecycle of Docker containers from installation to management on Arch Linux.
What was covered:

Installed Docker using Arch Linux package manager (pacman)
Enabled and started Docker as a background service using systemctl
Searched Docker Hub for available images via CLI
Pulled the official Nginx image from Docker Hub
Ran a named container with port mapping (8080:80) in detached mode
Verified running containers using docker ps with full status details
Tested container functionality by curling localhost and confirming Nginx HTML response
Executed commands inside a live container using docker exec
Ran a second Nginx container simultaneously on a different port (8081:80)
Managed full container lifecycle — stop, start and remove containers via CLI
Pulled and ran the official hello-world container to verify Docker installation integrity


Tech Stack

Arch Linux
Docker & Docker Compose
Nginx (reverse proxy + web server)
MySQL 8.0
PhpMyAdmin
OpenSSH
POSIX ACL
GRUB Bootloader
VMware Workstation Pro
Bash / CLI only


Skills Demonstrated

Linux system administration from scratch
Disk partitioning and filesystem management
User and group management with role-based access control
SSH hardening and security configuration
Container deployment and management
Reverse proxy configuration
Network security and least privilege principles
Technical documentation


About Me
Aspiring Cloud & DevOps Engineer currently following a structured learning roadmap.

🔗 LinkedIn:(https://www.linkedin.com/in/avishek-paudel-a72388413/)
📧 avishekspaudel12@gmail.com

Why I Built This
Built as part of my self-driven IT learning journey to develop deep hands-on skills in Linux server administration, virtualisation and container technologies. Rather than following a guided installer or GUI tool, every single configuration was typed manually, tested and verified through the command line. The aim was to understand infrastructure the way it works in real enterprise environments — from the ground up.
