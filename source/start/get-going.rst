Getting the robot running without any fuss
==========================================

Do you want to just get the robot to work? This is the place! This page will show you how to get the GUI going in (hopefully) under 10 minutes.
Please note - at the time of writing, the GUI code is not modular. This means it will currently not work for any robot you turn on without some tweaking.
If you **do** need help, please come find Angus Finch, a senior member of the robotics club or Mr. Nolan/Felix.

Installation
^^^^^^^^^^^^

First things first, make sure you have installed NodeJS and NPM:

``node -v && npm -v``

From there, we are able to install the RoboHUD project (make sure that you are in the right directory!):

``git clone https://github.com/CCGSRobotics/RoboHUD.git``

CD into the directory so we are in the right place:

``cd RoboHUD/``

Install all of the required packages with the following (this will install in the top directory and install in the server directory):

``npm install && cd Server/ && npm install && cd ..``

Getting the code on the Pi
^^^^^^^^^^^^^^^^^^^^^^^^^^

Now this is a tricky set of commands, but it is very useful to transfer files to the robot without any internet on the robot.
Open a new terminal window and SSH into the Pi (remember to change to its wireless network):

``ssh pi@192.168.100.1``

Check if there is an existing GUI folder in ~/:

``ls | grep "GUI"``

If there is no output from that command, run the following:

``mkdir GUI``

From there, you can CD into the GUI directory:

``cd GUI``

There is a **very** neat tool called scp, which uses the SSH technology to copy files across devices. Try using the following in the original terminal you opened:

``scp -r Server/ pi@192.168.100.1:~/GUI/``

Starting up
^^^^^^^^^^^

Go back to the SSH terminal and type in ``ls`` to make sure the files have been copied across. There should be a Server/ folder with some files in it.

Once again, use ``cd Server/`` to go into the project directory.

Use the command ``node server.js`` to start the compatability server

Return to the original terminal and run ``npm start``. The GUI should start, with the only thing left do do being the addition of a controller!