# Setting up WordPress Portfolio Websites

This guide demonstrates a possible system to setup WordPress-based portfolio websites. 

## System Requirements
### Hardware
The power of the hosting VM will vary based on the number of users it supports, but for the first 400 users it will need:

- 80-100 GB RAM (more is always better)
- 5 TB HDD/SSD (again, more is better)
- x64 or x86_64 processor (more GHz and cores are better)

### Software

- Ubuntu Server 16.04.2 LTS OR Debian Jessie (v8, "stable" branch) OR Debian Stretch (v9, "testing" branch)
- Docker container for each user
        - Apache
        - MySQL
        - PHP
        - WordPress
- Remote administration via SSH, keyed (passwordless) login
- Account registered in sudoers file

## Installation

Use `apt` to install packages. Setup ONE Docker container and clone it. Let users configure WordPress through the web interface. 
Configure DNS for each Docker container to route to a subdomain for each user. 

## Post-install

Setup automatic updates, remove test MySQL users for security, possibly change SSH port to something above 10,000, etc. 
