# Lab 1: Group-managment

## Objective

- Create and manage local users.
- Create and manage groups.
- Set and manage user passwords and account expiry.
- Configure sudo privileges for selected users.
- Verify user and group configurations.

## Steps

  ### 1. Create a new user
  ```bash
     sudo useradd alice
     sudo passwd alice
```
 -create anew user called alice and set password

  ### 2. Create a new group
  ```bash
     sudo groupadd developers
  ```
  ### 3. add user to group developers
  ```bash
     sudo usermod -aG developers alice
  ```
  ### 4 . verify user details 
  ```bash
   id alice
```
    - or
    - Display the contents of the /etc/group file and view member of developers group

 ### 5. change password expire date
  ```bash
     sudo usermod -e 2026-04-24 alice
  ```
 ### 6. verify password details
  ```bash 
      sudo cat /etc/shadow
```
  -Display the content of /etc/shadow file to verify info

 ### 7. Configure sudo for one of them
  ```bash
       sudo usermod -aG wheel alice
  ```
        
  ## Challenges
  - At first, I tried setting the password using:
```bash
sudo usermod -p password alice
```
-This stored the password as plain text in /etc/shadow, which is a security risk.
- To fix this, I switched to using the passwd command:
  ```bash
  sudo passwd alice
  ```
  -This stored the password securely as a hash instead of plain text.
