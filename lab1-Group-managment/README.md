# Lab 1: Group-managment

## Objective

- Create and manage local users.
- Create and manage groups.
- Set and manage user passwords and account expiry.
- Configure sudo privileges for selected users.
- Verify user and group configurations.

## Steps

  1. Create a new user
     sudo useradd alice
     sudo passwd alice
     #create anew user called alice and set password

  2. Create a new group
     sudo groupadd developers
  
  3. add user to group developers
     sudo usermod -aG developers alice

  4. verify user details 
      id alice
      or
      Display the contents of the /etc/group file and view member of developers group

  5. change password expire date
      sudo usermod -e 2026-04-24 alice

  6. verify password details
      sudo cat /etc/shadow
      Display the content of /etc/shadow file to verify info

  7. Configure sudo for one of them
       sudo usermod -aG wheel alice
       
        
     
     
