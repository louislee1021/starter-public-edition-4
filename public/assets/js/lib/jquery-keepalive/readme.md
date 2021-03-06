# jQuery keepalive Plugin #

Version: 1.0  
Date: 26 August 2010  
License: MIT License or GNU General Public License (GPL) Version 2  
Example at: [http://waynewalls.com/keepalive/](http://waynewalls.com/keepalive/)  

## BACKGROUND ##

This plugin sends ajax requests to the server at configurable intervals to keep
a PHP session from expiring.

## LIMITATIONS ##

none.


## keepalive DEPENDENCIES: ##

Requires jQuery v1.4;  there are no other dependencies.


## keepalive USAGE: ##

jQuery.keepalive is started automatically when the plug-in is included a page.

`$.keepalive.configure( config )`  
where config is an object containing keepalive options.

`$.keepalive.stop()  // stop the keepalive interval timer`

`$.keepalive.start( config )  // start the keepalive interval timer`  
where config is an optional object containing keepalive options.

`$.keepalive.toggleDisplay()  // toggle the keepalive status display`  
the status display is appended to the body element


## keepalive OPTIONS (type) [ default value ]: ##

`$.keepalive.options.url (string) [ "php/keepalive.php" ]`  
The URL to assign to the $.ajax() URL property

`$.keepalive.options.dataObject (object) [ { id:"keepalive" } ]`  
An object to be assigned to the $.ajax() data property

`$.keepalive.options.interval (integer) [ 300000 ]`  
The interval between requests to the server in milliseconds (default: 5-minutes)

`$.keepalive.options.timeout (integer) [ 20000 ]`  
An integer to be assigned to the $.ajax() timeout property

`$.keepalive.options.errorCallback (function()) [ null ]`  
A function that will be called when the keepalive $.ajax() request returns an
error.

`$.keepalive.options.successCallback (function()) [ null ]`  
A function that will be called after each successful keepalive $.ajax() request.


## keepalive PUBLIC METHODS: ##

`$.keepalive.configure( config )`  
Sets keepalive options where config is an object containing new options that
will act as default values for subsequent ajax requests.

`$.keepalive.stop()`  
Stop the keepalive interval timer.

`$.keepalive.start()`  
Start the keepalive interval timer.

`$.keepalive.toggleDisplay()`  
Toggles the keepalive status display.  The display is appended to the body
element.
