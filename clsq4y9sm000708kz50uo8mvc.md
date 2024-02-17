---
title: "🐍Day 13 - Basics of Python(Part - I)"
datePublished: Sat Feb 17 2024 13:49:49 GMT+0000 (Coordinated Universal Time)
cuid: clsq4y9sm000708kz50uo8mvc
slug: day-13-basics-of-pythonpart-i
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708171938824/06a3d2a9-3a94-4095-99d6-4c2519b6fb6d.png
tags: python, python3, devops, python-beginner, devops-journey, 90daysofdevops, trainwithshubham, vivekmoudekar

---

## 🐍What is Python ?

Python is a versatile and powerful programming language loved by beginners and experts alike. It's like a Swiss Army knife for coding because it can handle a wide range of tasks, from simple scripts to complex applications.

Imagine Python as a friendly language that speaks human-like syntax. Just like how you'd give instructions to a friend, you can tell Python what you want it to do, step by step, using plain language.

Here's a breakdown of why Python is so popular:

1. **<mark>Readable Syntax </mark>** : Python's syntax is clean and easy to understand, making it accessible for beginners. You don't need to be a coding genius to grasp its concepts.
    
2. **<mark>Versatility </mark>** : Python can be used for almost anything: web development, data analysis, artificial intelligence, automation, scientific computing, and more. It's like having a universal tool for various programming tasks.
    
3. **<mark>Cross-platform </mark>** : Python runs on different operating systems like Windows, macOS, and Linux, ensuring your code works regardless of the environment.
    
4. **<mark>Vibrant Community </mark>** : Python has a massive community of developers who contribute libraries, frameworks, and tutorials. If you ever get stuck, there's always someone willing to help.
    
5. **<mark>Interpreted Language </mark>** : Unlike languages like C++ or Java, Python doesn't need to be compiled before running. You can write code and execute it line by line, which accelerates development and debugging.
    
6. **<mark>Rich Ecosystem </mark>** : Python boasts a vast ecosystem of third-party libraries and frameworks that simplify complex tasks. Whether you're building a website with Django, analyzing data with Pandas, or creating neural networks with TensorFlow, there's a library for almost everything.
    

## **🐍How to Install Python ?**

**Installation of Python in Linux (Ubuntu):**

**<mark>Step 1 </mark>** : Open Terminal First things first, let's fire up the Terminal. You can do this by searching for "Terminal" in your application launcher.

**<mark>Step 2 </mark>** : Update Package Lists It's always a good idea and best practice to ensure your package lists are up to date before installing anything. Run the following command:

```plaintext
sudo apt-get update
Or                          #Both will Work
sudo apt update
```

**<mark>Step 3 </mark>** : Install Python Ubuntu typically comes with Python pre-installed, but we'll ensure we have the latest version. Run the following command to install Python 3:

```plaintext
sudo apt-get install python3
```

This command will install Python 3 and its dependencies. Once the installation is complete, you can verify the installation by typing:

```plaintext
python3 --version
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708171084849/79120117-102e-498e-8472-3c2baf3429c0.png align="center")

## 🐍Different Data Types in Python

* Primitive Data Structures
    
    you will say what is Primitive which can't be break further.
    

1. **Integer (**`int`**)**: Represents whole numbers without any fractional part.
    
    ```plaintext
     apples = 25   #int
    ```
    
2. **Float** : Represent real numbers with decimal point.
    
    ```plaintext
    Marks = 60.5   #float
    ```
    
3. **String (**`str`**)**: Represents a sequence of characters. `Single alphabet` or character is enclosed within <mark>(' ')</mark>single inverted comma and A `sequence of chracters` enclosed within <mark>(" ")</mark>Double inverted comma .
    
    ```plaintext
     name = "Vivek"
    sing = 'V'
    ```
    
4. **Boolean (**`bool`**)**: Represents either True or False.
    
    ```plaintext
    x = true
    y = false
    ```
    

* Non primitive Data structures
    

1. **List(**`list`**)** : Represents an ordered and sequential collection of items.It is heterogeneous means can store different data types. and it is mutable(can be changed).
    
    ```plaintext
    list_of_fruits = ["Banana",1,2,3,true,false] #This Method of Creating list is faster
    print(list_of_fruits)
    
    #Another way of making list is using function
    
    list_of_names = list() #this method will call the class
    print(type(list_of_names))
    ***********************************************************
    OPERATIONS IN LIST
    - append
    -clear
    -count
    -extend
    ```
    
2. **Tuple (**`tuple`**)**: Similar to lists, but immutable (cannot be changed once created).
    
    ```plaintext
     fruits = ("banana", "papaya")
    ```
    
3. **Dictionary (**`dict`**)**: Represents a collection of key-value pairs. Keys are always unique within a dictionary.
    
    ```plaintext
     d1 = {"name": "Vivek",
           "role": "Dev", 
           "city": "Pune"
          }
    ```
    
4. **Set (**`set`**)**: Represents an unordered collection of unique items. Duplicates are not allowed.
    
    ```plaintext
     numbers = {1, 2, 3,}
    ```
    
    ## 🚧Conclusion
    
    In wrapping up, understanding Python's various data types is like having a reliable map for your coding journey 🗺️. Each type has its own role, from numbers to text and more, helping you navigate through your programs with ease. So, embrace these tools, and let them guide you to success in your coding adventures! Happy coding! 🚀🐍😊
    

**Happy Learning**😊