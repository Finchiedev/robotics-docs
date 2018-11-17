./Server/server.js & ./App/index.html
==================

This is the main command layer that talks to the GUI and allows for a better user experience, allowing for automated, human-readable commands to be run.
When you press the start button on the GUI, this is what follows:

* The client writes *VIDEO* to the server
* The server recognises this command and executes the required camera streaming code
* After 1 second to allow time to execute, the client writes *START* to the server
* The server recognises this command and executes the required server code
* After 3 seconds to allow time to execute, the client begins to write servo instructions
