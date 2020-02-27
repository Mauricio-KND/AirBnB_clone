# AirBnB clone - The console

## Description

### Command interpreter to manage AirBnB objects

This is the first step towards building our first full web application: the AirBnB clone. This first step is very important because we will use what we build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help us to:

* Put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances.
* Create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file.
* Create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel.
* Create the first abstracted storage engine of the project: File storage.
* Create all unittests to validate all our classes and storage engine.

### What’s a command interpreter

Is the part of operating system that understands and executes commands that are entered interactively by a human being or from a program. Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

* Create a new object (ex: a new User or a new Place)
* Retrieve an object from a file, a database etc…
* Do operations on objects (count, compute stats, etc…)
* Update attributes of an object
* Destroy an object

## Table of Contents

1. [Installation](#Installation)
2. [Usage](#Usage)
3. [Authors](#Authors)

## Installation

```bash
git clone git@github.com:diego0096/AirBnB_clone.git
```

## Usage

### Interactive Mode

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update
(hbnb)
(hbnb)
(hbnb) quit
$
```

### Non Interactive Mode

```bash
$ echo "help" | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb) $
$
$ echo "create BaseModel" | ./console.py
(hbnb) f09bfbad-532d-4bbe-a2c1-815b1958f01e
(hbnb) $
$ echo "all" | ./console.py
(hbnb) [[BaseModel] (f09bfbad-532d-4bbe-a2c1-815b1958f01e) {'id': 'f09bfbad-532d-4bbe-a2c1-815b1958f01e', 'updated_at': datetime.datetime(2018, 6, 13, 23, 16, 30, 420332), 'created_at': datetime.datetime(2018, 6, 13, 23, 16, 30, 420300)}]
(hbnb) $
$ echo "destroy BaseModel f09bfbad-532d-4bbe-a2c1-815b1958f01e" | ./console.py
(hbnb) (hbnb) $
$ echo "all" | ./console.py
(hbnb) []
(hbnb) $
$
```

## Authors

The authors.

* Mauricio Drada Dávila
* Diego Felipe Quijano Zuñiga
