---
title: "📜Day 6 - File Permissions and Access Control Lists"
datePublished: Thu Feb 01 2024 11:23:38 GMT+0000 (Coordinated Universal Time)
cuid: cls34on8n000j09l6c0us8at4
slug: day-6-task-file-permissions-and-access-control-lists
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706782044166/317d3333-2459-420b-87d7-c63c4cd5f762.png
tags: devops, file-permission, 90daysofdevops, trainwithshubham, 90daysofdevops-chanllenge, access-control-list, devopscommunity, vivekmoudekar

---

The concept of Linux File permission and ownership is important in Linux. Here, we will be working on Linux permissions and ownership and will do tasks on both of them. Let us start with the Permissions.

1. ### 📜Create a simple file and do `ls -ltr` to see the details of the file
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706783607002/2811e555-b931-463f-9799-fd378be18e0b.png align="center")
    
2. ### **⚔Understanding the three Permission categories**
    

a. 🦹‍♀️Owner: The owner is the individual who created the file or directory. The owner has the highest level of control, including the ability to modify permissions, change ownership, and delete the file.

b. 👦🧒👨‍🦱Group: Every user in a Linux system belongs to at least one group. The group permissions apply to all users within that specific group, providing a convenient way to manage access for multiple users simultaneously.

c. 💂‍♂️Others: This category includes all users who are not the owner or part of the group associated with a file or directory. These permissions affect everyone else on the system.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706786311740/123c9151-2a7f-4eb3-ae0c-a898c3c175cf.png align="center")

1. ### **📏Changing Ownership with <mark>"chown</mark>**<mark>"</mark>:
    
    The "chown" command is used to change the ownership of a file or directory. For instance:
    

```plaintext
chown new_owner:new_group filename
```

Example: Suppose you have a file named "example.txt" currently owned by the user "user1" and the group "group1." To change the ownership to "user2" and the group to "group2," you would use the following command:

```plaintext
chown user2:group2 example.txt
```

After running this command, the ownership of "example.txt" would be transferred to "user2" and the group ownership to "group2."

It's important to note that the user executing the `chown` command must have the necessary permissions to change ownership of the file or directory.

1. ### 📏**Changing Group Permissions with <mark>"chgrp"</mark>**:
    
    To modify the group ownership of a file or directory, the "chgrp" command is used:
    

```plaintext
chgrp new_group filename
```

1. ### 📏**Modifying Other Users' Permissions with <mark>"chmod"</mark>**:
    
    To modify the group ownership of a file or directory, the "chgrp" command is used:
    
    ```plaintext
    chmod 777 filename
    # This will give file permission for Owner,group,others as READ WRITE and EXECUTE
    # read-4,Write-2,execute-1
    ```
    
    1. ### 📏**Checking Permissions with <mark>"ls -ltr"</mark>:**
        
        After modifying permissions, the "ls -ltr" command can be used to display detailed information about files and directories, including ownership and permissions.
        
        ```plaintext
        $ ls -ltr
        -rw-r--r-- 1 user1 group1 1024 Jan 1 10:00 filename
        ```
        
        In this example, the file "filename" is owned by "user1," belongs to the "group1" group, and has read and write permissions for the owner but only read permissions for the group and others.
        
    2. 📏**Advanced File Permissions with ACL**: Access Control Lists (ACL) provide a more granular approach to file permissions, allowing additional rules beyond the standard owner, group, and others. The <mark>"getfacl"</mark> command retrieves ACL information, while "setfacl" is used to define new ACL rules.
        
        Example:
        
        ```plaintext
        $ getfacl filename
        $ setfacl -m u:user2:rw- filename
        ```
        
        This example grants read and write permissions to "user2" specifically, supplementing the traditional owner, group, and others permissions.
        
    
    ### **🚧Conclusion:**
    
    Understanding and effectively managing file permissions is fundamental for maintaining a secure and organized Linux system. With the "chown," "chgrp," and "chmod" commands, administrators can control access on a per-user and per-group basis. Exploring ACL provides even more flexibility for intricate permission setups, enhancing the security of sensitive data within a Linux environment.
    

***this blog will help you discover new insights and learn something very exciting to do hands on.🙏***

**😊Happy Learning : )**