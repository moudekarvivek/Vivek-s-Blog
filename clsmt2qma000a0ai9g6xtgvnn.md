---
title: "⚔Day 12 - Linux , Git and Github Commands Cheat-Sheet"
datePublished: Thu Feb 15 2024 05:54:03 GMT+0000 (Coordinated Universal Time)
cuid: clsmt2qma000a0ai9g6xtgvnn
slug: day-12-linux-git-and-github-commands-cheat-sheet
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1707976158823/0d2042d7-0549-48a3-a804-884e44ae50c1.png
tags: linux, github, git, linux-for-beginners, linux-basics, 90daysofdevops, trainwithshubham, 90daysofdevops-chanllenge, vivekmoudekar

---

This cheat sheet provides quick access to essential Linux commands organized into categories like navigation, file management, search, permissions, system management, and Git/GitHub workflows. With clear descriptions, modes, and examples, users can efficiently perform tasks such as navigating directories, managing files, searching text, handling permissions, monitoring processes, and version controlling with Git. Ideal for both beginners and experienced users, this resource enhances productivity and proficiency in Linux command line operations and version control practices.

# Linux Commands Cheat Sheet\*\* 🐧

## **Navigation:** 🗺️

### **<mark>cd</mark>**

1. Usage : <mark>To change Directories</mark>
    
2. Modes :
    
    📍 `~` : Home directory.
    
    📍 `..` : Previous directory.
    

Example:

* " cd ~ " : *Change to the Home Directory*
    
* " cd .. " : *Change to the previous Directory*
    

---

## **File Management:** 📁

### **<mark>ls</mark>**

1. Usage : <mark>List Directory Contents.</mark>
    

Modes :

📍 `-a` : Show hidden files

📍 `-l`: Use a long listing format

Example:

* " ls -a " : *Lists all files, including hidden ones*.
    
* " ls -l " : *Displays detailed information about files.*
    

### **<mark>mkdir</mark>**

1. Usage : <mark>Make Directory</mark>
    
2. Modes :
    
    📍`-p`: Create parent directories if they do not exist.
    

Example:

* " mkdir `new_folder`": *Creates a new directory named "new\_folder".*
    
* " mkdir -p parent\_folder/sub\_folder ": *Creates nested directories.*
    

### <mark>rm</mark>

1. Usage : <mark>Remove files or directories.</mark>
    
2. Modes :
    
    📍 `-r` : Recursively remove directory.
    
    📍 `-f` : Force removal without confirmation.
    

Example:

* " rm file.txt " : *Deletes a file named "file.txt".*
    
* " rm -rf directory " : *Removes a directory and its contents forcefully.*
    

### **<mark>cp</mark>**

1. Usage : <mark>Copy files or directories.</mark>
    
2. Modes :
    
    📍 `-r`: Copy directories recursively.
    
    📍`-u`: Update - copy only when source is newer than destination.
    
    Example:
    
    * " cp file.txt destination/ " : *Copies "file.txt" to the "destination" directory.*
        
    * " cp -ru source/ destination/ ": *Copies newer files from source to destination.*
        

### **<mark>mv</mark>**

1. Usage : <mark>Move or rename files or directories.</mark>
    

Example:

* " mv file.txt new\_location/ " : *Moves "file.txt" to "new\_location".*
    
* " mv old\_name.txt new\_name.txt " : Renames "old\_name.txt" to "new\_name.txt".
    

### **<mark>cat</mark>**

1. Usage : <mark>Display file content.</mark>
    
2. Modes :
    
    📍`-n` : Number all output lines.
    

Example:

* " cat file.txt " : *Displays content of "file.txt".*
    
* " cat -n file.txt " : *Displays content with line numbers.*
    

---

# **Search and Filter:** 🔍

### **<mark>grep</mark>**

1. Usage : <mark>Search Text.</mark>
    
2. Modes:
    
    📍`-i`: Ignore case distinctions.
    
    📍`-v`: Invert match.
    

Example:

* " grep "keyword" file.txt " : *Searches for "keyword" in "file.txt".*
    
* " grep -i "word" file.txt " : *Searches ignoring case.*
    

---

## **Permissions and Security:** 🔒

### **<mark>chmod</mark>**

1. Usage : <mark>Change file permissions.</mark>
    
2. Modes :
    
    📍`u/g/o` : User/group/others
    
    📍`+/-` : Add/remove Permission
    

Example:

* " chmod u+x [script.sh](http://script.sh) " : *Adds execute permission to the owner.*
    
* " chmod go-w file.txt " : *Removes write permission from group and others.*
    

---

## **System Management:** ⚙️

### <mark>sudo</mark>

1. Usage : <mark>Execute a command with superuser privileges</mark>.
    

Example:

**sudo apt-get update**

## <mark>top</mark>

1. Usage : <mark>Display and manage running processes.</mark>
    
2. Modes :
    
    📍`-u` : Display processes for a specific user.
    

Example:

* " top " : *Displays processes in real-time.*
    
* " top -u username " : *Shows processes for a specific user.*
    

## **<mark>df</mark>**

1. Usage : <mark>Report file system disk space usage.</mark>
    
2. Modes :
    
    📍`-h` : Human-readable format.
    

Example:

* " df -h " : *Displays disk space usage in a human-readable format.*
    
* " df -hT " : *Shows disk space usage with filesystem type.*
    

---

## **Downloading and Archiving:** 📦

## <mark>wget</mark>

1. Usage : <mark>Download files from the internet.</mark>
    

Example:

* " wget [http://example.com/file.txt](http://example.com/file.txt) " : Downloads "file.txt" from the web.
    
* " wget -O filename [http://example.com/file.txt](http://example.com/file.txt) " : Saves downloaded file with a specific name.
    

## <mark>tar</mark>

1. Usage : To zip or compress file handle tar archieves.
    
2. Modes :
    
    📍`-x` : Extract files from an archieve.
    
    📍`-z` : Filter the archive through gzip.
    

Example:

* " tar -xvf archive.tar.gz " : Extracts files from a tarball.
    

" tar -czf archive.tar.gz directory/ " : Creates a gzip-compressed tarball of a directory.

---

# **Git and GitHub Commands Cheat Sheet** 🚀

## **Version Control:** 🔄

1. **<mark>git init</mark>**
    
    * Usage: Initialize a new Git repository.
        
    * Example: `git init`
        
2. **<mark>git clone</mark>**
    
    * Usage: Clone a repository into a new directory.
        
    * Example: `git clone <repository_url>`
        
3. **<mark>git add</mark>**
    
    * Usage: Add file contents to the index.
        
    * Example: `git add file.txt`
        
4. **<mark>git commit</mark>**
    
    * Usage: Record changes to the repository.
        
    * Modes:
        
        * `-m`: Specify commit message.
            
    * Example: `git commit -m "Commit message"`
        
5. **<mark>git push</mark>**
    
    * Usage: Update remote refs along with associated objects.
        
    * Example: `git push origin main`
        
6. **<mark>git pull</mark>**
    
    * Usage: Fetch from and integrate with another repository or a local branch.
        
    * Example: `git pull origin main`
        
7. **<mark>git branch</mark>**
    
    * Usage: List, create, or delete branches.
        
    * Example: `git branch feature`
        
8. **<mark>git checkout</mark>**
    
    * Usage: Switch branches or restore working tree files.
        
    * Example: `git checkout feature`
        
9. **<mark>git merge</mark>**
    
    * Usage: Join two or more development histories together.
        
    * Example: `git merge feature`
        
10. **<mark>git log</mark>**
    
    * Usage: Show commit logs.
        
    * Example: `git log`
        
11. **<mark>git status</mark>**
    
    * Usage: Show the working tree status.
        
    * Example: `git status`
        
12. <mark>git remote</mark>
    
    * Usage: Manage set of tracked repositories.
        
    * Modes:
        
        * `-v`: List remote URLs.
            
    * Example: `git remote -v`
        

***This cheat sheet covers commands for Linux, Git and GitHub. providing a quick reference for revision , share and spread the knowledge! 🌟***

Happy Learning 😊:)