---
attachments: [Clipboard_2020-12-17-07-12-52.png]
tags: [Lessons]
title: Coding Club 1
created: "2020-12-14T13:57:00.018Z"
modified: "2020-12-17T07:12:52.430Z"
---

# Coding Club 1

## Recap

- **30 Days of python [YouTube Playlist](https://www.youtube.com/watch?v=RGor6fssp6c&list=PLEsfXFp6DpzQjDBvhNy5YbaBx9j-ZsUe6)**

  - [ ] Python 3.8.x intallation [link](https://www.youtube.com/watch?v=RGor6fssp6c)
  - [ ] Numbers, Variables and Strings [link](https://www.youtube.com/watch?v=pLniTMTW0vE)
  - [ ] Lists & Dictionaries [link](https://www.youtube.com/watch?v=NqacT1CjkmQ&list=PLEsfXFp6DpzQjDBvhNy5YbaBx9j-ZsUe6&index=3)
  - [ ] Iteration & Loops [link](https://www.youtube.com/watch?v=iTa1ZnWdIS0&list=PLEsfXFp6DpzQjDBvhNy5YbaBx9j-ZsUe6&index=4)
  - [ ] Conditionals & Control Flow [link](https://youtu.be/ZbdXzqO0uLo)
  - [ ] String Formatting & F Strings [link](https://youtu.be/pZIwn52DEsU)
  - [ ] Functions & Python Modules [link](https://youtu.be/W9PN20FE3sE)
  - [ ] Importing - Internal & External [link](https://youtu.be/yhF6wAgs3_E)
  - [ ] Send Email & Read Inbox [link](https://youtu.be/6DD4IOHhNYo)
  - [ ] Files - Create, Read & Download [link](https://youtu.be/Rf9ShctbZZQ)
  - [ ] Classes and State [link](https://youtu.be/cRJgLAA2KeI)

## Abstract Data Types

- What is abstract data types?
-

## Abstraction in Programming

- Abstraction as Modeling
- Abstraction as Encapsulation

## Topics covered

- how do we model real world problem into a computer programm
- Concept of Computational Problem
- Automation

### String Methods

```python
# capitalize() : converts the first character to uppercase
greeting = "hello world. hello geo!"
greeting = greeting.capitalize()
print(greeting)
```

```python
# lower() : Converts string into lower case
greeting = "HELLO WORLD"
greeting = greeting.lower()
print(greeting)
```

```python
# split(): Splits the string at the specified separator, and returns a list
greeting = "Hello world"
greeting = greeting.split(" ")
print(greeting)
```

```python
# join() : Joins the elements of an iterable to the end of the string
words = ['Hello', 'world']
greeting = ",".join(words)
print(greeting)
```

```python
# join() : Joins the elements of an iterable to the end of the string
dist  = {"Hello": "Hola"}
greeting = "Hello John Doe!"
translated_greeting = greeting.translate(dist)
print(translated_greeting)
```

## Computational thinking and abstraction

![Computational thinking and abstraction](../attachments/Clipboard_2020-12-17-07-12-52.png)

## Putting it all together

Its time to put all of these skills together so here is the scenario. A manager in your troop has recently arrived. He has to send 2x geographic technicians to support an external unit, but they should have python programming knowledge and be class 1 qualified. We are going to create a python program to help the manager shortlist appropriate technicians from a pool of his technicians.

```python
class GeoTech:
    def __init__(self, name, service_number, qualifications):
        self.name = name
        self.service_number = service_number
        self.qualifications = qualifications

    def can_deploy(self):
        if(('Class1' in self.qualifications) and ('JavaScript' in self.qualifications)):
            return "Yes"
        else:
            return "No"


if __name__ == "__main__":
    geotech_pool = []

    geo1 = GeoTech('Joe', 30048377, [
        'Class1', 'Class2', "Python", "JavaScript"])
    geo2 = GeoTech('John', 30048377, ['Class2', "Python", "JavaScript"])
    geo3 = GeoTech('Doe', 30048377, ['Class1', 'Class2',  "JavaScript"])
    geo4 = GeoTech('Jake', 30048377, ['Class2'])

    geotech_pool.append(geo1)
    geotech_pool.append(geo2)
    geotech_pool.append(geo3)
    geotech_pool.append(geo4)

    # List name and number of soldier
    for geo in geotech_pool:
        print(f"{geo.name} - {geo.can_deploy()}")

    # Lets say the requirement is to find Class1 with Python knowledge
    # we will add new method in our GeoTech class:
    # can_deploy ? return true or false

    class GeoTech:

        def __init__(self, name, service_number, qualifications):
            self.name = name
            self.service_number = service_number
            self.qualifications = qualifications

        def can_deploy(self):
            if(('Class1' in self.qualifications) and ('JavaScript' in self.qualifications)):
                return "Yes"
            else:
                return "No"
```

