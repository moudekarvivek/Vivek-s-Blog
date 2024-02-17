---
title: "🐍Day 14- Python Data Types and Data Structures for DevOps"
datePublished: Sat Feb 17 2024 18:22:23 GMT+0000 (Coordinated Universal Time)
cuid: clsqeosvg00000al32nkphv3n
slug: day-14-python-data-types-and-data-structures-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708193089339/02b093fa-2604-4325-8377-cffd70837961.png
tags: python, python3, devops, python-beginner, 90daysofdevops, trainwithshubham, vivekmoudekar

---

## 📍Python Data types

Data types are the classification or categorization of data items. It represents the kind of value that tells what operations can be performed on a particular data. Since everything is an object in Python programming, data types are actually classes and variables are instance (object) of these classes. Python has the following data types built-in by default: Numeric(Integer, complex, float), Sequential(string, lists, tuples), Boolean, Set, Dictionaries, etc.

To check what is the data type of the variable used, we can simply write:

```python
# Let us take some example to understand briefly
apples = 20  #Integer(int)
marks = 60.5 #Float(float)
name = "Vivek" #String(str)
is_raining = False #boolean Note: this is case sensetive
list_var = [1, 2, 3]
tuple_var = (1, 2, 3)
dict_var = {"key": "value"}

# To check the data type
print(type(apples)) # Output: <class 'int'>
print(type(marks))  # Output: <class 'float'>
print(type(name))   # Output: <class 'str'>
print(type(is_raining)) # Output: <class 'bool'>
print(type(list_var)) # Output: <class 'list'>
print(type(tuple_var)) # Output: <class 'tuple'>
print(type(dict_var)) # Output: <class 'dict'>
```

## 📍Data Structures

Data Structures are a way of organizing data so that it can be accessed more efficiently depending upon the situation. Data Structures are fundamentals of any programming language around which a program is built. Python helps to learn the fundamental of these data structures in a simpler way as compared to other programming languages.

1. **<mark>Lists</mark>**
    
    * Python Lists are just like the arrays, declared in other languages which is an ordered collection of data. It is very flexible as the items in a list do not need to be of the same type.
        
    * Mutable (able to modified after creation).
        
    * Allows duplicate elements.
        
    * Accessed by index.
        
    * Syntax: `[item1, item2]`.
        
2. **<mark>Tuple</mark>**
    
    * Python Tuple is a collection of Python objects much like a list but Tuples are immutable in nature i.e. the elements in the tuple cannot be added or removed once created. Just like a List, a Tuple can also contain elements of various types.
        
    * Immutable (can't be modified once created).
        
    * Allows duplicate elements.
        
    * Accessed by index.
        
    * Syntax: `(item1, item2)` .
        
3. **<mark>Dictionaries</mark>**
    
    * Python dictionary is like hash tables in any other language with the time complexity of O(1). It is an unordered collection of data values, used to store data values like a map, which, unlike other Data Types that hold only a single value as an element, Dictionary holds the key:value pair. Key-value is provided in the dictionary to make it more optimized.
        
    * Mutable (able to modified after creation).
        
    * can Accessed by key.
        
    * Any datatype can be used.
        
    * Syntax: `{key1: value1, key2: value2}`.
        

## ✔Tasks

1. ### **Give the Difference between List, Tuple and set. Do Hands-on and put screenshots as per your understanding.**
    
    1. **<mark>Lists</mark>** 📜:
        
        * 📋 Ordered collections of items.
            
        * 🔄 Mutable: You can add, remove, or modify elements after creation.
            
        * 🔧 Created using square brackets `[]`.
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708191147274/a970a98f-1fb7-4ac7-aa27-2d022b0dff67.png align="center")
            
    2. **<mark>Sets</mark>** 🎭:
        
        * 🎈 Unordered collections of unique items.
            
        * 🔄 Mutable: You can add or remove elements after creation, but you cannot modify individual elements.
            
        * 🛠️ Created using curly braces `{}` or the `set()` function.
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708191544221/0bbccc21-aec7-4f68-bf7b-e1a6f5164881.png align="center")
            
    3. **<mark>Tuples</mark>** 🔄:
        
        * 📦 Ordered collections of items.
            
        * 🔒 Immutable: Once created, you cannot add, remove, or modify elements.
            
        * 🔒 Created using parentheses `()`.
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708191638162/77eaa0a8-8ea5-4936-953a-2a3acd66c9a3.png align="center")
            
    
    In summary:
    
    1. 📜 Lists are like dynamic checklists where you can change, add, or remove items as needed.
        
    2. 🎭 Sets are like a bag of unique items where you can throw in new ones or take them out, ensuring each item is unique.
        
    3. 🔄 Tuples are like fixed-size packages where once sealed, the contents cannot be changed.
        
        1. ### **Task2- Create below Dictionary and use Dictionary methods to print your favorite tool just by using the keys of the Dictionary.**
            
        
        ```python
        fav_tools = {
            1: "Linux",
            2: "Git",
            3: "Docker",
            4: "Kubernetes",
            5: "Terraform",
            6: "Ansible",
            7: "Chef"
        }
        
        # Print your favorite tool using its corresponding key
        favorite_tool_key = 2  # Assuming your favorite tool is Git and its key is 2
        favorite_tool = fav_tools.get(favorite_tool_key)
        
        if favorite_tool:
            print("My favorite tool is:", favorite_tool)
        else:
            print("Sorry, your favorite tool is not found in the dictionary.")
        ```
        
        ###   
        3\. Task -3 **Create a List of cloud service providers** `eg. cloud_providers = ["AWS","GCP","Azure"]` & Write a program to add `Digital Ocean` to the list of cloud\_providers and sort the list in alphabetical order.
        
        ```python
        # List of cloud service providers
        cloud_providers = ["AWS", "GCP", "Azure"]
        
        # Add Digital Ocean to the list
        cloud_providers.append("Digital Ocean")
        
        # Sort the list in alphabetical order
        cloud_providers.sort()
        
        # Print the sorted list
        print("Sorted list of cloud service providers:")
        for provider in cloud_providers:
            print(provider)
        ```
        
        This code will output the list of cloud service providers sorted alphabetically, with "Digital Ocean" included:
        
        ```python
        Sorted list of cloud service providers:
        AWS
        Azure
        Digital Ocean
        GCP
        ```
        
        ### **🚧Conclusion**
        
        Python's data types and data structures empower DevOps practitioners with efficient tools for managing and manipulating data, enhancing productivity.
        
    
    Happy Learning 😊