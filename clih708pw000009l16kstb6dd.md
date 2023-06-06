---
title: "Day 15 Task: Python Libraries for DevOps"
datePublished: Sun Jun 04 2023 09:00:21 GMT+0000 (Coordinated Universal Time)
cuid: clih708pw000009l16kstb6dd
slug: day-15-task-python-libraries-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/95YRwf6CNw8/upload/b46f16d705aaa8d80be3acc1450d6105.jpeg
tags: aws, python, json, devops, yaml

---

### Reading JSON and YAML in Python

* As a DevOps Engineer, you should be able to parse files, be it txt, json, yaml, etc.
    
* You should know what all libraries one should use in Python for DevOps.
    
* Python has numerous libraries like `os`, `sys`, `json`, `yaml` etc that a DevOps Engineer uses in day-to-day tasks.
    
* Ref
    
* %[https://youtu.be/whNFPBEI-wM] 
    
* %[https://youtu.be/Pq54CmgAwpw] 
    
* ## Tasks
    
    1. Read a json file `services.json` kept in this folder and print the service names of every cloud service provider.
        
    
    ```python
    output
    
    aws : ec2
    azure : VM
    gcp : compute engine
    ```
    
    2\. Read YAML file using python, file `services.yaml` and read the contents to convert yaml to json
    
* Ans 1 and 2
    
* ```python
          import json
          import yaml
          
          json_file = r"path\services.json"
          yaml_file = r"path\services.yaml"
          
          # Load data from JSON file
          with open(json_file, 'r', encoding='utf-8') as f:
              json_data = json.load(f)
          
          print("JSON:\n", json_data)
          
          # Load data from YAML file
          with open(yaml_file, "r") as stream:
              try:
                  yaml_data = yaml.safe_load(stream)
                  print("YAML:\n", yaml_data)
              except yaml.YAMLError as exc:
                  print(exc)
    ```
    

```json
{
    "Services":{
        "debug": "on",
        "aws":{
            "name": "EC2",
            "type": "pay-per hour",
            "instances": 500,
            "count": 500
        },
        "azure":{
            "name": "VM",
            "type": "pay-per hour",
            "instances": 500,
            "count": 500
        },
        "gcp":{
            "name": "Compute Engine",
            "type": "pay-per hour",
            "instances": 500,
            "count": 500
        }
    }
}
```

```yaml
---
services:
  debug: 'on'
  aws:
    name: EC2
    type: pay per hour
    instances: 500
    count: 500
  azure:
    name: VM
    type: pay per hour
    instances: 500
    count: 500
  gcp:
    name: Compute Engine
    type: pay per hour
    instances: 500
    count: 500
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685868448503/66abd5ff-89cd-4870-aa2e-b6c970077bf0.png align="center")