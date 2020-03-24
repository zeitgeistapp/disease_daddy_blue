# Daddy Blue WebServices

Project DaddyBlue is the server infrastructure to give access to all the Smartphone APPs, WebPages and other Applications we require.

It is build in currently 3 blocks:

* the registration and login
* the account handling 
* the appointments

To give maximum data security we implemented them into one project, but distributable according to the requirements.

So the registration could run (without the user data and the laboratory results) on a central server.

In a federal goverment structure, the accounts will be accordingly on national or federal servers.

The appointments, for the sake of reliability and accessiveness, could be even inside the trucks or placed localy inside the laboratories.

## Installation and Setup

### Standard configuration

#### File location

* Server: ```/opt/zeitgeist/daddyblue/daddyblue.jar```
* Configuration File: ```/etc/zeitgeist/daddyblue.config```
* Log folder: ```/var/lib/zeitgeist/daddyblue/```

#### Configuration file

This is an example configuration file, where all the webservices are activated on a single machine. (not recommended, but for testing really handy)

```
#######################################
# listeners for the server
#######################################
host=0.0.0.0
port=7272

#######################################
# activated web services
#######################################
registry=true
account=true
testers=true
laboratory=true

#######################################
# mobile phone settings
#######################################
# the short message text to be sent. 
# !!! DON'T FORGETT TO PLACE THE {otp} into the text !!!
sms_text=Ihr Zeitgeist Aktivierungscode lautet {otp}
# the value is a regular expression to validate the number
valid_phone_numbers=\+491(5|6|7)[0-9]{8,9}
# in pipeline: smseagle, smscreator
# today implemented twilio
sms_provider=twilio

#######################################
# where to place the log protocolls
#######################################
log_path=/var/lib/zeitgeits/daddyblue/

```


## WebService API

Please find below the WebService API (we need someone to draw it more professionally! Volunteer required!)

![Page 1](doc/DaddyBlue_Communication_1.jpeg?raw=true "Page 1")

![Page 2](doc/DaddyBlue_Communication_2.jpeg?raw=true "Page 2")

![Page 3](doc/DaddyBlue_Communication_3.jpeg?raw=true "Page 3")

![Page 4](doc/DaddyBlue_Communication_4.jpeg?raw=true "Page 4")

![Page 5](doc/DaddyBlue_Communication_5.jpeg?raw=true "Page 5")


