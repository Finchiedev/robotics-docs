---
description: 'With all of the dependencies installed, what comes next?'
---

# Basic implementation of servos

Now that you are in the `Driving/` directory, let's take a look around. Run the command

```bash
ls
```

And you'll see the following output:

* Servos/ - The folder containing all servo configurations as a `.csv` file
* dynamixels.py - A file containing the `Dynamixel` class and setup utilities
* server.py - A file that implements dynamixels.py by hosting a `UDP` server

Make a new file called &lt;your name&gt;Server.py with the following code:

```bash
touch <your name>Server.py
# For example, Bob would do
touch bobServer.py
```

Now that this file exists, you can start editing the code. Open the file in a text editor of your choice, or by using this command:

```bash
nano <your name>Server.py
```

From there, we can start creating the code to interface with the robot. Add the following line to the file you have just created:

```python
from dynamixels import initialise_dynamixel
```

This will tell Python to include the `initialise_dynamixel` function for later use. Looking inside dynamixels.py, the definition of the function includes some information about its usage. 

