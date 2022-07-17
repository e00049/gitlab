#Step 01: Update system & install dependencies

sudo apt upgrade -y
sudo apt install -y ca-certificates curl openssh-server tzdata

#Step 02: Add the GitLab CE Repository

curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash

#Step 03: Add repository contents to

sudo cat /etc/apt/sources.list.d/gitlab_gitlab-ce.list

#Step 04: Install GitLab CE on Ubuntu 18.04

sudo apt update
sudo apt install gitlab-ce -y

#step 05: Edit the GitLab configuration file to set hostname and other parameters:

sudo vi /etc/gitlab/gitlab.rb
    
    external_url 'http://gitlab.example.com'  to Your Server Name
    
#step 06: When done, start your GitLab instance by running the following command

sudo gitlab-ctl reconfigure

#Step 07:  Default User name and Password: 
User name : root
password:  sudo cat /etc/gitlab/initial_root_password


Ref: https://computingforgeeks.com/how-to-install-gitlab-ce-on-ubuntu-linux/
