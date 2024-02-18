---
title: "📚Day 15- Python Libraries for DevOps"
datePublished: Sun Feb 18 2024 14:50:46 GMT+0000 (Coordinated Universal Time)
cuid: clsrmkijy000409jyf4ftfufk
slug: day-15-python-libraries-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708267703782/bad78b48-079f-4a5a-a1c3-27550d5db1b5.png
tags: python, json, python3, yaml, python-libraries, python-beginner, 90daysofdevops, trainwithshubham, vivekmoudekar

---

## **✔JSON and YAML in Python**

* As a DevOps Engineer you should be able to parse files, be it txt, json, yaml, etc.
    
* You should know what all libraries one should use in Pythonfor DevOps.
    
* Python has numerous libraries like `os`, `sys`, `json`, `yaml` etc that a DevOps Engineer uses in day to day tasks.
    

## ✔**Advantages of YAML:**

1. **<mark>Human- Readable and Writeable</mark>**
    
    YAML's syntax is designed to be human-friendly and easily readable, featuring indentation-based structure and minimal punctuation. This readability enhances collaboration and understanding, particularly in scenarios where non-technical stakeholders are involved.
    
2. **<mark>Expressiveness and Conciseness</mark>**
    
    YAML offers a concise and expressive format for representing complex data structures, including lists, dictionaries, and nested objects.reduces verbosity and enhances readability, especially for configuration files and data serialization.
    
3. **<mark>Data Serialization</mark>**
    
    YAML supports serialization of complex data types, including objects, arrays, and nested structures, without the need for additional transformation. This makes it suitable for serializing and deserializing data between different programming languages and environments.
    
4. **<mark>Integration with Configuration Management</mark>**
    
    YAML is commonly used for configuration files in software development, deployment, and infrastructure management. Its human-readable syntax and support for hierarchical configurations make it well-suited for defining settings, parameters, and dependencies in applications and systems.
    

## ✔**Advantages of JSON:**

1. **<mark>Simplicity and Familiarity</mark>**
    
    JSON's syntax is straightforward and closely resembles JavaScript object notation, making it intuitive and easy to understand for developers familiar with JavaScript or similar languages.
    
2. **<mark>Lightweight and Fast</mark>**
    
    JSON is a lightweight format, which means it's efficient in terms of both storage and transmission. Its simplicity also contributes to faster parsing and serialization, making it ideal for use cases where performance is critical.
    
3. **<mark>Widespread Adoption</mark>**
    
    JSON has gained widespread adoption across various domains, including web development, APIs, and configuration files. Its popularity ensures extensive support across programming languages and platforms, making it a versatile choice for data interchange.
    
4. **<mark>Standardization</mark>**
    
    JSON has a standardized format and parsing rules, ensuring consistency in how data is represented and processed across different systems.
    
    ⚡ *In summary, while JSON excels in simplicity, performance, and interoperability, YAML stands out for its readability, expressiveness, and suitability for configuration management.*
    

### ✔Tasks:

1. ### **<mark>Create a Dictionary and Write to a JSON File.</mark>**
    

```python
import json

# Create a dictionary
data = {
    "name": "Vivek",
    "age": 23,
    "city": "Pune"
}

# Define the file path where you want to save the JSON file
file_path = "data.json"

# Write the dictionary to a JSON file

with open(file_path, "w") as json_file:
    json.dump(data, json_file)

print("Dictionary has been written to data.json successfully!")
```

### In this code:

1. We create a dictionary named `data` containing some key-value pairs (in this case, the name, age, and city).
    
2. We specify the file path where we want to save the JSON file (`data.json`).
    
3. We open the file in write mode (`"w"`) using the `open()` function along with a context manager (`with` statement) to ensure that the file is properly closed after writing.
    
4. We use `json.dump()` function to write the contents of the dictionary `data` into the JSON file specified by `json_file`.
    
5. Finally, we print a message indicating that the dictionary has been successfully written to the JSON file.
    

After running this code, you should find a file named `data.json` in your current working directory, containing the dictionary data in JSON format.

1. ### **<mark>Read a .json file</mark>**`services.json` <mark> kept in this folder and print the service names of every cloud service provider.</mark>
    

```python
import json

# Specify the path to the JSON file
file_path = "services.json"

# Read the JSON file
with open(file_path, "r") as json_file:
    services_data = json.load(json_file)

# Print service names of every cloud service provider
for provider, service in services_data.items():
    print(f"{provider}: {service}")
```

In this code:

1. We specify the path to the JSON file "services.json".
    
2. We use the `open()` function to open the JSON file in read mode (`"r"`) along with a context manager (`with` statement).
    
3. We use `json.load()` function to load the contents of the JSON file into the `services_data` dictionary.
    
4. We iterate through the items of the `services_data` dictionary using a `for` loop, where each item represents a cloud service provider and its corresponding service name.
    
5. Inside the loop, we print the provider name and its associated service name.
    

Make sure that the "services.json" file is in the same directory as your Python script, or you need to provide the correct path to the file.

1. ### <mark>Read a YAML File and Convert it to JSON</mark>
    

```python
import yaml
import json

# Specify the path to the YAML file
yaml_file_path = "services.yaml"

# Read the YAML file
with open(yaml_file_path, "r") as yaml_file:
    yaml_data = yaml.safe_load(yaml_file)

# Convert YAML data to JSON
json_data = json.dumps(yaml_data, indent=4)

# Print the JSON data
print(json_data)
```

In this code:

1. We import the `yaml` and `json` modules.
    
2. We specify the path to the YAML file ("services.yaml").
    
3. We use the `open()` function to open the YAML file in read mode (`"r"`) along with a context manager (`with` statement).
    
4. We use [`yaml.safe`](http://yaml.safe)`_load()` function to load the contents of the YAML file into the `yaml_data` dictionary. `safe_load()` is used to safely load YAML data without executing arbitrary code.
    
5. We use `json.dumps()` function to convert the `yaml_data` dictionary to a JSON-formatted string. We also specify `indent=4` to format the JSON data with indentation for better readability.
    
6. Finally, we print the JSON data.
    

This will read the YAML file, convert its contents to JSON, and print the JSON-formatted data. You can then use this JSON data as needed, such as writing it to a JSON file or passing it to other functions for further processing.

Happy Learning😊