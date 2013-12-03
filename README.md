# Django 1.6 Template

## Overview
This is a modified and repurposed version of this project [https://github.com/twoscoops/django-twoscoops-project](https://github.com/twoscoops/django-twoscoops-project).  Also, I've trimmed the instructions to work with a *nix system (not Windows).

The goal is to have a standardized baseline Django 1.6 application skeleton to build web applications from.

## Requirements
The documentation below assumes you're using [virtualenv](http://www.virtualenv.org/ "Virtualenv") and [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/ "Virtualenvwrapper") to manage versions and dependencies within different development environments.  In order to properly develop this application you should have the following installed:

* [Virtualenv](http://www.virtualenv.org/ "Virtualenv")
* [Virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/ "Virtualenvwrapper")

## Setup

* [Create a Virtual Environment](#create-virtualenv)
* [Clone the Template](#clone-template)
* [Install Dependencies](#install-dependencies)
* [Run Server](#run-server)

### [Create a Virtual Environment](id:anchor-create-a-virtual-environment)

In a terminal, create your virtual environment using virtualenvwrapper commands.  Here we'll name it ```django16```, but you may want to change it to something that makes more sense for your this environment.

    $ mkvirtualenv django16

You should see something similar to the following:

    New python executable in django16/bin/python
    Installing Setuptools ...done.
    Installing Pip ...done.

…and your prompt should now look something like this:

    (django16)$

Note: See the [Virtualenvwrapper Docs](http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html "Virtualenvwrapper Docs") for more commands.

### [Clone the Template](id:anchor-clone-the-template)

To create a project using this template, open a terminal and navigate to the place where you want to keep your project, let's say it's **~/projects/**.

    (django16)$ cd ~/projects

Assuming you are still in the context of the django16 virtual environment, let's clone the project into a directory called **projectName**:

    (django16)$ git clone https://github.com/dereknutile/django-1.6-template.git projectName

### [Install Dependencies](id:anchor-install-dependencies)

First, make sure you are in the directory for the project you just made:

    (django16)$ cd projectName

You should now be in the ~/projects/**projectName** directory.


Installing dependencies is done using PIP and is relative to your environment.  The environment requirements are listed within requirements directory with a file name like _{environment}.txt_.

To install requirements on your development system, use PIP to reference the development configuration file:

    (django16)$ pip install -r requirements/development.txt

### [Run Server](id:anchor-run-server)

First, initialize the SQLITE database.  Note: you may be asked to define the superuser/admin.

    (django16)$ python project/manage.py syncdb
    
Initialize the [SOUTH](http://south.readthedocs.org/) database migrations:

    (django16)$ python project/manage.py migrate --initial

Run the server ...

    (django16)$ python project/manage.py runserver    

Test it out: [http://127.0.0.1:8000](127.0.0.1:8000).