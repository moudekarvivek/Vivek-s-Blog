---
title: "Day 2 -Getting Started with Linux Commands: A Quick Guide : Part I"
datePublished: Tue Jan 30 2024 17:48:49 GMT+0000 (Coordinated Universal Time)
cuid: cls0nkahp000109l43d498svy
slug: day-2-getting-started-with-linux-commands-a-quick-guide-part-i
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706636776414/5c086564-0f68-4ecd-acb8-31e4d30311b1.avif

---

## **Linux Architecture**

Linux is a robust and versatile operating system that powers a significant portion of the computing world, from servers and embedded systems to desktops and mobile devices. In this blog post, we will take a closer look at the architecture that underlies the Linux operating system.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706548068021/bb3c953c-9d11-4e76-9c45-49ebb2c10142.png align="center")

## **Kernel:**

At the heart of Linux is the kernel, the core component that manages system resources, facilitates communication between hardware and software, and provides essential services. The kernel is the powerhouse of a computer's operating system, wielding complete control over every aspect of the system. It's the unsung hero behind the scenes! 💻

We Can't directly command to the kernel as it can understand the machine language so for that **Shell** helps to communicate to kernel also known as CLI.

### **Shell:**

The shell is your interactive gateway to the operating system, translating user commands into a language the kernel comprehends. Think of it as the mediator, accepting human-readable instructions and making things happen. 🤖💬

### **Linux Shell Scripting:**

Shell scripting is the art of creating programs run by a Linux shell. These scripts, often considered scripting languages, empower DevOps engineers to perform tasks like file manipulation, program execution, and text printing—all from the command line. 📜🚀

## **Introduction**

Linux commands are powerful tools that allow users to interact with the operating system through the command line interface (CLI). In this article, we'll cover some basic Linux commands to help you navigate and perform common tasks.

### **🚀Basic Linux Commands**

### 1.⚜️***File Commands***

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1706636065213/7903e8a2-8a23-473e-a56e-92085fc881f8.png align="center")

### **2.⚜️*Directory commands***

mkdir dirName # make a new directory 'dirName'

mkdir .Newdir # make a hidden directory (also . before a file to make it hidden)

mkdir A B C D #make multiple directories at the same time

mkdir /home/user/Mydir # make a new folder in a specific location

mkdir -p A/B/C/D # make a nested directory

pwd #This command will display the full path to the current directory.

cd path\_to\_directory #change directory to the provided path

cd ~ or just cd #change directory to the home directory

cd - # Go to the last working directory.

cd .. # change directory to one step back.

cd ../.. # Change directory to 2 levels back.

## **Creating Nested Directories**

To create nested directories, the `mkdir` command is employed. The `-p` option allows you to create parent directories if they don't exist.

This example creates a nested directory structure A/B/C/D/E. The `-p` option ensures that all parent directories are created, even if some of them are missing.

## **Conclusion**

These basic Linux commands are just the tip of the iceberg. As you delve deeper into the world of Linux, you'll discover a plethora of commands and options to streamline your workflow.

***I'm confident that this blog will prove to be valuable, helping you discover new insights and learn something enriching*** .🙏

😊Happy Learning : )