# Lab 2: file-permission-acl

## Objective

- Create directories /projectX, /projectY. 
- Give different users/groups access with chmod and setfacl. 
- Use umask to control default permissions. 

## Steps

  ### 1. Create two directories by user (gemy)
  ```bash
     mkdir projX projY
```
[![](Images/1.jpg)](Images/1.jpg)


  ### 2. change projX directory owner , group and SUID
  ```bash
     sudo chgrp developers projX
     sudo chown omar projX
     chmod u+s projX
  ```
[![](Images/3.jpg)](Images/3.jpg)

  ### 3. add permission to alice on projY 
  ```bash
     sudo setfacl -m u:alice:rwx projY
  ```
[![](Images/4.jpg)](Images/4.jpg)


  ### 4. control default permission 
   #### 1. temporary
  ```bash
   umask 002
  ```
  - when create directory (777-umask) and file (666-umask)
    
[![](Images/7.jpg)](Images/7.jpg)

  #### 2. permenant for one user 
  - modify bashrc file
    
[![](Images/6.jpg)](Images/6.jpg)
    
  #### 3. permenant for all users  
  
  - modify /etc/profile 


    
 
  -This stored the password securely as a hash instead of plain text.



