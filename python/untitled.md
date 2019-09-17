---
description: >-
  What will you need? Where can you find these resources? Who can you ask for
  help?
---

# Setting up your environment

Of course, there's not much point in having software that interfaces with hardware without letting your software interface with your hardware. To get a basic setup going, you will need:

* A USB2Dynamixel
* Any Robotis Dynamixel servo
* A laptop, preferably running linux \(you will need to change the port names in `dynamixels.py`\)
* An internet connection

{% hint style="info" %}
If you can attend a CCGS Robotics session, you can ask for a test bed, which includes all of the resources you need to get started. Additionally, you will find a lot of people there who are more than happy to help!
{% endhint %}

The first thing you want to do is clone the repositories with the following code:

```bash
git clone https://github.com/CCGSRobotics/RoboHUD
git clone https://github.com/ROBOTIS-GIT/DynamixelSDK
```

And move them somewhere else:

```bash
mkdir ~/GUI
mv RoboHUD DynamixelSDK ~/GUI
cd ~/GUI
```

From there, the next step is to install the `DynamixelSDK`

```bash
cd DynamixelSDK/python
python3 setup.py build && sudo python3 setup.py install
```

With the Python setup complete, you can now move into the `Driving` directory

```bash
cd ~/GUI/RoboHUD/Server/Driving
```

