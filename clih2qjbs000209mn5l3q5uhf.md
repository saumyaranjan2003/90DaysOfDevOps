---
title: "Day 14 Task: Python Data Types and Data Structures for DevOps"
datePublished: Sun Jun 04 2023 07:00:50 GMT+0000 (Coordinated Universal Time)
cuid: clih2qjbs000209mn5l3q5uhf
slug: day-14-task-python-data-types-and-data-structures-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/ieic5Tq8YMk/upload/060ab49f8366a1f1eeb9b171f152c852.jpeg
tags: aws, python, azure, devops, vscode

---

### Data Types

* Data types are the classification or categorization of data items. It represents the kind of value that tells what operations can be performed on a particular data.
    
* Since everything is an object in Python programming, data types are actually classes and variables are instance (object) of these classes.
    
* Python has the following data types built-in by default: Numeric(Integer, complex, float), Sequential(string,lists, tuples), Boolean, Set, Dictionaries, etc
    

To check what is the data type of the variable used, we can simply write: `your_variable=100` `type(your_variable)`

### Data Structures

Data Structures are a way of organizing data so that it can be accessed more efficiently depending upon the situation. Data Structures are fundamentals of any programming language around which a program is built. Python helps to learn the fundamental of these data structures in a simpler way as compared to other programming languages.

* Lists Python Lists are just like the arrays, declared in other languages which is an ordered collection of data. It is very flexible as the items in a list do not need to be of the same type
    
* Tuple Python Tuple is a collection of Python objects much like a list but Tuples are immutable in nature i.e. the elements in the tuple cannot be added or removed once created. Just like a List, a Tuple can also contain elements of various types.
    
* Dictionary Python dictionary is like hash tables in any other language with the time complexity of O(1). It is an unordered collection of data values, used to store data values like a map, which, unlike other Data Types that hold only a single value as an element, Dictionary holds the key:value pair. Key-value is provided in the dictionary to make it more optimized
    
    ## Tasks
    
    1. Give the Difference between List, Tuple and set. Do Handson and put screenshots as per your understanding.
        
        List, Tuple, and Set are three different data structures in Python with distinct characteristics. Here are the differences between them:
        
        1. List:
            
            * Mutable: Lists are mutable, which means you can add, remove, or modify elements after the list is created.
                
            * Ordered: Elements in a list are ordered and can be accessed using indices.
                
            * Allows duplicates: Lists can contain duplicate elements.
                
            * Syntax: Defined using square brackets \[\].
                
        2. Tuple:
            
            * Immutable: Tuples are immutable, which means you cannot modify elements once a tuple is created.
                
            * Ordered: Like lists, tuples are ordered and can be accessed using indices.
                
            * Allows duplicates: Tuples can contain duplicate elements.
                
            * Syntax: Defined using parentheses () or without any delimiter.
                
        3. Set:
            
            * Mutable: Sets are mutable, which means you can add or remove elements after the set is created.
                
            * Unordered: Elements in a set are unordered, and their order may change.
                
            * Unique elements: Sets only contain unique elements. Duplicate elements are automatically eliminated.
                
            * Syntax: Defined using curly braces {} or the `set()` function.
                
        
        In summary, lists are mutable, ordered, and allow duplicates; tuples are immutable, ordered, and allow duplicates; sets are mutable, unordered, and contain only unique elements. The choice of which data structure to use depends on the specific requirements of your program.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685861299276/149207e9-bba3-4e08-9ba3-4fee66ec1c63.png align="center")
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685861331860/ccf563b4-b6fb-4691-a8a2-797fa042007d.png align="center")
        
    2. Create below Dictionary and use Dictionary methods to print your favourite tool just by using the keys of the Dictionary
        
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
        
        favorite_tool = fav_tools[3]
        print(favorite_tool)
        
        -> Docker
        ```
        
    3. Create a List of cloud service providers
        
        ```python
        cloud_providers = ["AWS","GCP","Azure"]
        ```
        
    4. Write a program to add `Digital Ocean` to the list of cloud\_providers and sort the list in alphabetical order.
        
        \[Hint: Use keys to built-in functions for Lists\]
        
        ```python
        cloud_providers = ["AWS","GCP","Azure"]
        cloud_providers.append("Digital Ocean")
        print(sorted(cloud_providers))
        
        ->['AWS', 'Azure', 'Digital Ocean', 'GCP']
        ```