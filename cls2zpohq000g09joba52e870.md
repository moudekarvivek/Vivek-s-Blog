---
title: "💻Day 4 Task: Basic Linux Shell Scripting for DevOps Engineers 🚀"
datePublished: Thu Feb 01 2024 09:04:28 GMT+0000 (Coordinated Universal Time)
cuid: cls2zpohq000g09joba52e870
slug: day-4-task-basic-linux-shell-scripting-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706775026994/08525bae-df16-486e-b43a-61bf09f1b2d7.png
tags: linux, devops, 90daysofdevops, trainwithshubham, tws

---

# 🔍 Understanding the Basics:

### **🧠** What is the Kernel?

The kernel is like the brain of your Linux system. It makes sure all the different parts (software and hardware) work together smoothly, just like a conductor leading an orchestra.

**🔍 What Does It Do?**

1. **Talks to Hardware:** It helps your computer software communicate with the physical parts, ensuring they understand each other.
    
2. **Memory Manager:** Manages the computer's memory to keep things running efficiently.
    
3. **Task Organizer:** Keeps an eye on all the tasks your computer is doing, making sure everything runs on time.
    
4. **Device Translator:** Acts as a universal translator between your computer and its accessories like printers or USB drives.
    
5. **Security Guard:** Protects your computer by controlling who can access what, like a virtual security guard.
    
6. **🔒 Security and Stability:** Imagine the kernel as your computer's bodyguard. It protects against unwanted guests (hackers) and makes sure everything runs smoothly without crashing.
    
    **🚀 Always Improving:** Just like your phone gets updates, the Linux kernel gets better over time. Developers from around the world work together to make sure it's always improving, bringing new features and fixing problems.
    
    **🌐 Conclusion:** The Linux kernel is like the secret sauce that makes your computer awesome. It's not something you see, but it's working hard behind the scenes to keep everything in harmony.
    
    ### **🐚 What is a Shell?**
    
    Think of a shell as the user-friendly translator between you (the user) and your computer's operating system. It's like a command center that takes your human-readable commands and turns them into something the computer understands.
    
    ### **🚀 What Does It Do?**
    
    1. **Interpreter of Commands:** You give commands in plain language, and the shell translates them into instructions the computer can execute.
        
    2. **Environment Customizer:** It lets you personalize your computing environment, changing settings and making your computer work the way you want.
        
    3. **Task Automator:** With scripts, the shell can automate repetitive tasks, saving you time and effort.
        
    
    🌐 **Introduction:** Ever wished your computer could do things on its own? Enter Linux Shell Scripting – it's like giving your computer a magic wand to follow your commands automatically. Let's uncover the mystery in simple terms.
    
    ### **🤖 What is Shell Scripting?**
    
    Shell scripting is the art of creating programs run by a Linux shell. These scripts, often considered scripting languages, empower DevOps engineers to perform tasks like file manipulation, program execution, and text printing—all from the command line. 📜🚀
    
    **🔧 Why Use Shell Scripts?**
    
    1. **No More Repetition:** Ever get tired of typing the same commands? A script lets you do it all at once.
        
    2. **Save Time:** Automate tasks, like organizing files or installing software, with just one command.
        
    3. **Your Computer, Your Rules:** Personalize how your computer behaves by creating your own set of instructions.
        
    
    **📜 Anatomy of a Shell Script:** Think of a shell script like a cooking recipe. You list the steps (commands) in order, and your computer follows them one by one.
    
    ### **⚙️ Getting Started:**
    
    1. **Write Your To-Do List:** Open a simple text editor and jot down your tasks.
        
    2. **Save with .sh:** Save your file with a .sh ending (e.g., [`tasks.sh`](http://mytasks.sh)) to let the computer know it's a special script.
        
    3. **Make It Ready:** Run a simple command to make your script ready for action.
        
    
    **🚀 Examples of Shell Scripting Tasks:**
    
    1. **Hello World Script:**
        
    
    ```bash
    #!/bin/bash
    echo "Hello, World!"
    ```
    
    1. **User Input Script:**
        
        ```bash
        #!/bin/bash
        echo "What's your name?"
        read name
        echo "Hello, $name!"
        ```
        
        ### *🤔What is* `#!/bin/bash?` *can we write* `#!/bin/sh` *as well?*
        
        `'#!/bin/bash'` and '`#!/bin/sh'` are known as shebangs, and they indicate the path to the interpreter that should be used to execute the script. Both are valid, but there are some distinctions between them.
        
    
    1. `#!/bin/bash`**:**
        
        * This shebang specifies that the Bash shell should be used as the interpreter.
            
        * Bash (Bourne Again SHell) is an enhanced version of the traditional Bourne shell (`/bin/sh`) and includes additional features.
            
    2. `#!/bin/sh`**:**
        
        * This shebang specifies the default system shell (often the Bourne shell) as the interpreter.
            
        * It may be a little more limited in features compared to Bash but is generally more lightweight.
            
        
        ### **🙄Choosing Between Them:**
        
        * If your script uses specific features that are Bash-specific, use `#!/bin/bash`.
            
        * If you want to ensure maximum portability and compatibility with various Unix-like systems, including those where `/bin/sh` might not be Bash, consider using `#!/bin/sh`.
            
        
        In many cases, especially for simple scripts, using `#!/bin/sh` is sufficient. However, if you're taking advantage of Bash-specific features, it's better to be explicit and use `#!/bin/bash`.
        

### **⚡*Write a Shell Script which prints "I will complete #90DaysOfDevOps challenge*"**

```bash
#!/bin/bash
echo "I will complete #90DaysOfDevOps challenge"
 #Bash script that prints a commitment message for the #90DaysOfDevOps challenge.
```

### **⚡*Write a Shell Script to take user input, input from arguments and print the variables.***

```bash
#!/bin/bash
echo "Pls Enter your age: "
read age
echo "Your age is ${age}"
```

***Note:*** Save this script in a file, for example, `first.sh`. [Give exe](http://script.sh/)cute permissions to the script using the `chmod 777 first.sh` or chmod +x first.sh command.

You can then run this script through ./ or bash

```plaintext
./first.sh argument
or
bash first.sh argument
```

### **⚡*Write an Example of If else in Shell Scripting by comparing 2 numbers.***

```bash
#!/bin/bash

# Get user input for two numbers
echo "Enter the first number:"
read num1

echo "Enter the second number:"
read num2

# Compare the two numbers
if [ "$num1" -eq "$num2" ]; then
 echo "The numbers are equal."
elif [ "$num1" -gt "$num2" ]; then
 echo "The first number ($num1) is greater than the second number ($num2)."
else
 echo "The second number ($num2) is greater than the first number ($num1)."
fi
```

***Note:*** Save this script in a file, for example, `compare.sh`. Give Execute permissions to the script using the `chmod 777 compare.sh` or chmod +x compare.sh command.

### 🚧***Conclusion:***

Embrace the magic of Linux Shell Scripting—your shortcut to automating tasks. Whether it's `#!/bin/bash` for flair or `#!/bin/sh` for simplicity, let your scripts be your digital accomplice. So, go ahead, write your commands, and watch your computer follow your lead. Happy scripting! 🚀💡

***this blog will help you discover new insights and learn something very exciting to do hands on.🙏***

**😊Happy Learning : )**