# Django 1.6 Template

## Overview
This is a modified and repurposed version of this project [https://github.com/twoscoops/django-twoscoops-project](https://github.com/twoscoops/django-twoscoops-project).

The goal is to have a standardized baseline Django 1.6 application skeleton to build web applications from.

## Requirements
The application uses Python and Django tools like [virtualenv](http://www.virtualenv.org/ "Virtualenv") and [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/ "Virtualenvwrapper") to manage versions and dependencies within different development environments.  In order to properly use this application you must have the following installed:

* [Virtualenv](http://www.virtualenv.org/ "Virtualenv")
* [Virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/ "Virtualenvwrapper")

## Setup

* [Clone the Template](#clone-template)
* [Create a Virtual Environment](#create-virtualenv)
* [Install Django within the Virtual Environment](#install-django)
* [Install Dependencies](#install-dependencies)

### [Clone the Template](id:clone-template)

To create a project using this template, open a terminal and type the following:

    $ django-admin.py startproject --template=https://github.com/dereknutile/django-1.6-template/zipball/master --extension=py,rst,html project

### [Create a Virtual Environment](id:anchor-create-virtualenv)

In a terminal, create your virtual environment using virtualenvwrapper commands.  Here we'll name it ```django16```, but you may want to change it to something that makes more sense for your application.

    $ mkvirtualenv django16

You should see something similar to the following:

    New python executable in django16/bin/python
    Installing Setuptools ...done.
    Installing Pip ...done.

…and your prompt should now look something like this:

    (django16)$

See the [Virtualenvwrapper Docs](http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html "Virtualenvwrapper Docs") for more commands.

 
### [Install Django within the Virtual Environment](id:anchor-install-django)

To install Django in the new virtual environment, run the following command::

    (django16)$ pip install django

### [Install Dependencies](id:anchor-install-dependencies)

Installing dependencies is done using PIP and is relative to your environment.  The environment requirements are listed within requirements directory with a file name like ```{environment}.txt```.

To install requirements on your development system:

    (django16)$ pip install -r requirements/development.txt
