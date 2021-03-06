---
description: What is the Dynamixel class? What does it do?
---

# The Dynamixel class

## What is the Dynamixel class?

The Dynamixel class is a Python class that abstracts the [DynamixelSDK ](https://github.com/ROBOTIS-GIT/DynamixelSDK)into a modular, control-table based class supporting value reading, writing and both protocols with one U2D2.

{% hint style="info" %}
Every Dynamixel has a _control table_, which is a list of addresses that correspond to pieces of information relating to the servo. To find the control table for a specific Dynamixel, visit the [Robotis e-Manual](http://emanual.robotis.com/) site and select your servo.
{% endhint %}

The way it works is by using an individual CSV for each servo that is based upon the relevant e-Manual control table documentation, allowing systems to be based on the _Data Name_ of something, rather than the hard-coded address for that on a particular type of servo.

What this means is that, for example, you want to set the Counter Clockwise Angle Limit on an MX-28, the old code would require the following lines to access [Address 8](http://emanual.robotis.com/docs/en/dxl/mx/mx-28/#ccw-angle-limit):

```python
dxl_comm_result, dxl_error = packetHandler.write2ByteTxRx(portHandler, ID, 8, 4095)
dxlErrors(dxl_comm_result, dxl_error)
```

Which, as you can see, means having to modify the code every time a new servo is implemented. With the new code, the addresses are mapped out on a per-servo basis, allowing for modularity in the code. Instead of specifying the address, packet handler and packet size, a servo that has already been initialised as `dynamixel` can be accessed with this much neater code:

```python
dynamixel.write_value('CCW Angle Limit')
```

Of course, the example of the new server is much easier to understand, allows for more modularity and produces cleaner code. A new servo simply requires a new CSV, generated by the client and sent through TCP. The CSV generated for an XL-320 servo \(which is documented [here](http://emanual.robotis.com/docs/en/dxl/x/xl320/#control-table-of-eeprom-area)\) would be:

{% embed url="https://gist.github.com/Finchiedev/178822fc754f140f15105f76c3100949" %}

As you can see, every single option is part of this file, and stored in the Dynamixel object for use by local and external functions.

