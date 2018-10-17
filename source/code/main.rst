./Main.js
=========
Declarations
^^^^^^^^^^^^
This is the first file that the Electron program runs when you execute **npm start**. Let's go through it, piece by piece. ::

    const {
    app,
    BrowserWindow
    } = require('electron')

The purpose of the code above is to make sure that NodeJS knows what Electron is when it starts up. It calls app and BrowserWindow as "constructors", used by NodeJS to integrate packages.
This is the equivalent of the Python3 code: ::
    import app, BrowserWindow from Electron
