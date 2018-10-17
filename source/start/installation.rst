Installing the project
======================
Installing NodeJS
^^^^^^^^^^^^^^^^^
It is a good idea to install NodeJS if you wish to follow along with this tutorial. All you have to do is go to the `NodeJS downloads page <https://nodejs.org/en/download/>`_ and install the relevant files.
Then follow the instructions to finish setup. Check you have the language installed by typing the following into a shell: ::
    node -v
    npm -v

If there are numbers appearing underneath the commands, NodeJS and NPM have been installed. Now to use them!

Electron guides
^^^^^^^^^^^^^^^
Electron has a `quick start guide <https://github.com/electron/electron-quick-start>`_ that demos how to get a simple Electron app running.
To get started, simply type the following commands: ::
    git clone https://github.com/electron/electron-quick-start.git
    cd electron-quick-start
    npm install
    npm start

There is also a more extensive demo, which includes some things that Electron can do to imitate native apps.
This can be found at `Electron API demos <https://github.com/electron/electron-api-demos>`_, but this documentation will not cover it in detail.

Installation of the GUI
^^^^^^^^^^^^^^^^^^^^^^^
By this point you would have poked around the very primitive Electron demo. Or maybe not. Your choice.
To install the robotics GUI, use the following commands: ::
    git clone https://github.com/Finchiedev/robotics-gui.git
    cd robotics-gui
    npm install

Before starting the application, make sure that you have Python installed. Chances are, if you're reading this guide & following along, you have a Linux distro booted.
If you have no idea what that is, please ask someone to help you with setting up a laptop. If you would rather use another OS, the installation of Python is relatively easy.
**On Windows:**
Simply go to the `Python downloads page <https://www.python.org/downloads/>`_ and find the relevant Windows installer.
Run the .exe file, and make sure that the box labelled *Add Python to your PATH* IS CHECKED. This is incredibly important for later
Done! Congratulations on installing Python on your machine!

**On MacOS:**
Tricked you! Python3 should be installed by default. Simply go to spotlight, type in terminal and check that Python is installed by typing: ::
    python3
If it works, there should be a sign that looks like **>>>**. Type quit() to exit.

Installation breakdown
^^^^^^^^^^^^^^^^^^^^^^^
Above you were shown the basic workflow for installing an Electron application. Let's break it down.

The first part of the code uses Git: ::

    git clone <project url>.git

This gives your command line the following instructions:

1. Use package **Git** to complete this operation
2. The function for Git to perform is to clone (Download) a project
3. Git should download from the specified URL and make it into a folder called <project-name>

I highly recommend learning more about Git with the `"Pro Git" book <https://git-scm.com/book/en/v2>`_. Even if you have used before, it is worth reading, as you are bound to learn something!
It also helps develop skills for a real-world professional programming environment

The next commands are relatively simple:

* cd <project-name> [Tells the computer to go to that folder]
* npm install [Uses NPM (*Node Package Manager*) to install the required files]
* npm start [Instructs NPM to run the start script]
