# 0x00. AirBnB clone - The console
The image shows the basic concept for this project
![AirBnB clone concept](https://github.com/jacobgbemi/AirBnB_clone/blob/main/airbnb_concept.png)

## Project Description
- This is a project to create AirBnB clone.
- [console](https://github.com/jacobgbemi/AirBnB_clone/blob/main/console.py) - contains the codes for command interpreter
- [models](https://github.com/jacobgbemi/AirBnB_clone/tree/main/models) - is a folder containing the Parent class (BaseModel), the subclasses (User, Amenity, State, Place, Review) and the engine folder hosting the Filestorage.
- [tests](https://github.com/jacobgbemi/AirBnB_clone/tree/main/tests) - a folder containing all the unittest for the codes.

## Description of command line interpreter
### Installation
```
git clone git@github.com:gjdame/AirBnB_clone.git
cd AirBnB_clone
```
### - How to start it
Interactive Mode
```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```

Non Interactive Mode
```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

### - How to use it
In the console.py, you will find the following commands:
- ```help```
  - Usage: ```help```
  - Funtion: ```displays available commands```

- ```create```
  - Usage: ```create <class>```
  - Funtion: ```creates new object (ex. a new User, Place)```

- ```update```
  - Usage: ```User.update('123', {'name' : 'Jacob'})```
  - Funtion: ```updates attribute of an object```

- ```destroy```
  - Usage: ```User.destroy('123')```
  - Funtion: ```destroys specified object```

- ```show```
  - Usage: ```User.show('123')```
  - Funtion: ```retrieves an object from a file, a database```

- ```all```
  - Usage: ```User.all()```
  - Funtion: ```displays all objects in class```

- ```count```
  - Usage: ```User.count()```
  - Funtion: ```returns count of objects in specified class```

- ```quit```
  - Usage: ```quit```
  - Funtion: ```exits command interpreter```

### - Examples
- Creating user
```
$ ./console.py
(hbnb) create User 
9c2cdd8c-262e-4da5-aefb-a9c8c525eabb
(hbnb)
(hbnb) update User
** instance id missing **
(hbnb) User.show("9c2cdd8c-262e-4da5-aefb-a9c8c525eabb")
[User] (9c2cdd8c-262e-4da5-aefb-a9c8c525eabb) {'id': '9c2cdd8c-262e-4da5-aefb-a9c8c525eabb', 'created_at': datetime.datetime(2022, 9, 5, 12, 44, 9, 42912), 'updated_at': datetime.datetime(2022, 9, 5, 12, 44, 9, 42927)} 
(hbnb) 
(hbnb) User.update("9c2cdd8c-262e-4da5-aefb-a9c8c525eabb", "fisrt_name", "Gbemi")
(hbnb) User.show("9c2cdd8c-262e-4da5-aefb-a9c8c525eabb")
[User] (9c2cdd8c-262e-4da5-aefb-a9c8c525eabb) {'id': '9c2cdd8c-262e-4da5-aefb-a9c8c525eabb', 'created_at': datetime.datetime(2022, 9, 5, 12, 44, 9, 42912), 'updated_at': datetime.datetime(2022, 9, 5, 12, 44, 9, 42927), 'fisrt_name': '"Gbemi"'}                                                       
(hbnb)
(hbnb) quit
$
```

### Unittest
- Run the entire: 
  ```
  $ python3 unittest -m discover tests
  ```
- Run single file test:
  ```
  $ python3 unittest -m tests/test_console.py
  ```
  
  ### Tools
- - PEP8/Coding style: [pycodestyle 2.8.0](https://pypi.org/project/pycodestyle/) || [Google Style Python Docstring](http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html)
- - Python 3.8.0
- - Text edotor: Vim
- - OS: Ubuntu 20.04(Focal)
- - VM: VirtualBox and Vagrant (To install Vagrant, follow these [steps](https://github.com/jacobgbemi/zero_day#readme))


  ### Authors
  - Conrad Obi 
  - Gbemi Jacob Adebayo | [Twitter](https://twitter.com/helpthemgrowup) | [LinkedIn](https://www.linkedin.com/in/gbemi-jacob-adebayo/)
