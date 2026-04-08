# Day 7 — Variables, JSON & YAML

## Key Focus
- Understanding variables in programming
- Basics of Python data structures
- Working with JSON format
- Understanding YAML syntax and usage

---

## Topics Covered

### 1. Introduction
- Overview of variables and data formats used in DevOps  
- Importance of structured data in automation and configuration  

---

### 2. Variables & Python Data Structures
- Variables are used to store data values  
- Python data structures help organize and manage data  

Examples:

```python
# String
name = "Pawan"

# Integer
age = 25

# List (ordered collection)
skills = ["AWS", "DevOps", "Linux"]

# Tuple (immutable collection)
tools = ("Docker", "Kubernetes")

# Dictionary (key-value pairs)
person = {
  "name": "Pawan",
  "age": 25,
  "skills": ["AWS", "DevOps"]
}
```

---

### 3. JSON (JavaScript Object Notation)
- Lightweight data format used for data exchange  
- Widely used in APIs and configuration  

Example:

```json
{
  "name": "Pawan",
  "skills": ["AWS", "DevOps"],
  "experience": 3
}
```

---

### 4. YAML (YAML Ain’t Markup Language)
- Human-readable data format  
- Commonly used in Kubernetes, Ansible, CI/CD  

Example:

```yaml
name: Pawan
skills:
  - AWS
  - DevOps
experience: 3
```

👉 YAML is cleaner and more readable than JSON  

---

### 5. Converting Dictionary → JSON → YAML

#### Python Dictionary:

```python
person = {
  "name": "Pawan",
  "age": 25,
  "skills": ["AWS", "DevOps"]
}
```

#### Converted to JSON:

```json
{
  "name": "Pawan",
  "age": 25,
  "skills": ["AWS", "DevOps"]
}
```

#### Converted to YAML:

```yaml
name: Pawan
age: 25
skills:
  - AWS
  - DevOps
```

👉 Same data, different formats — used in different tools  

---

## Hands-On Practice

Today I performed the following:

- Created variables using Python  
- Practiced string, integer, list, tuple and dictionary  
- Converted dictionary data into JSON format  
- Wrote YAML manually  
- Compared JSON and YAML structures  

---

## What Confused Me Today

**Problem:**  
Understanding difference between JSON and YAML  

**Reason:**  
Both represent similar data but syntax differs  

**Fix:**  
Practiced writing same data in both formats  

**Lesson:**  
Focus on structure rather than syntax differences  

---

## Interview Questions I Can Answer

- What are variables in programming?  
- What are Python data structures?  
- What is JSON and where is it used?  
- What is YAML and why is it preferred?  
- Difference between JSON and YAML?  

---

## What I Learned (Big Picture)

- Variables store data used in automation  
- JSON is widely used in APIs  
- YAML is heavily used in DevOps tools  
- Same data can be represented in multiple formats  

---

## What I Would Improve

- Practice complex JSON structures  
- Learn YAML deeply for Kubernetes  
- Work with real configuration files  

---

## Tomorrow’s Plan

- Continue next section  
- Practice JSON and YAML more  
- Try real DevOps configuration examples
