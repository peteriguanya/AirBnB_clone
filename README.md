![💻AirBnB_clone_-_The_console (3)](https://user-images.githubusercontent.com/110534527/218313247-92a48af5-6e70-49cf-b3c8-49814378634f.png)

![GitHub contributors](https://img.shields.io/github/contributors/Ckimatu/AirBnB_clone)
![GitHub last commit](https://img.shields.io/github/last-commit/Ckimatu/AirBnB_clone)

# Project Description

This is the first step towards building our first full web application: the AirBnB clone.

# Description of the command interpreter

The interface of the application has a limited number of accepted commands that were solely defined for the usage of the AirBnB website.
This command line interpreter serves as the frontend of the web app.

The following actions can be performed:
* Creating new objects (ex: a new User or a new Place)
* Retrieving an object from a file, a database etc…
* Doing operations on objects (count, compute stats, etc…)
* Updating attributes of an object
* Destroying an object

# How to start it

*Installation*

1. You will need to clone the repository of the project from Github
2. After cloning the repository you will have a folder called AirBnB_clone, that will contain several files that allow the program to work, including:
* /console.py : The main executable of the project, the command interpreter.
* models/engine/file_storage.py: Contains a class that serializes instances to a JSON file and deserializes JSON file to instances
* models/__ init __.py: A unique FileStorage instance for the application
* models/base_model.py: Contains a class that defines all common attributes/methods for other classes.
* models/user.py: Contains a user class that inherits from BaseModel
* models/state.py: Contains a state class that inherits from BaseModel
* models/city.py: Contains a city class that inherits from BaseModel
* models/amenity.py: Contains an amenity class that inherits from BaseModel
* models/place.py: Contains a place class that inherits from BaseModel
* models/review.py: Contains a review class that inherits from BaseModel

# How to use it

It can work in two different modes:
Interactive and Non-interactive.

* Interactive mode - the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again to wait for a new command. This can go indefinitely as long as the user does not exit the program.

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

* Non-interactive mode - the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode, no prompt will appear, and no further input will be expected from the user.

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

# Format of Command Input

* Non-interactive mode: in order to give commands to the console, these will need to be piped through an echo.

* Interactive Mode: the commands will need to be written with a keyboard when the prompt appears and will be recognized when an enter key is pressed (new line). As soon as this happens, the console will attempt to execute the command through several means or will show an error message if the command didn't run successfully. In this mode, the console can be exited using the CTRL + D combination, CTRL + C, or the command quit or EOF.

# Arguments 

Most commands have several options or arguments that can be used when executing the program. In order for the Shell to recognize those parameters, the user must separate everything with spaces.

*Example*

```

user@ubuntu:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@ubuntu:~/AirBnB$ ./console.py

```

# Commands available

 | Command | Description |
 | ------- | ----------- |
 | quit or EOF | Exits the program | By itself |
 | help | Provides a text describing how to use a command |
 | create | Creates a new instance of a valid Class, saves it (to the JSON file) and prints the id |
 | show | Prints the string representation of an instance based on the class name and id |
 | destroy | Deletes an instance based on the class name and id (saves the change into a JSON file) |
 | all | Prints all string representation of all instances based or not on the class name |
 | update | Updates an instance based on the class name and id by adding or updating attribute (saves the changes into a JSON file) |
 | count | Retrieve the number of instances of a class |





