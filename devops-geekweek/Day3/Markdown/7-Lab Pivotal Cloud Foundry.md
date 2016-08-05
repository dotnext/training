# Lab Pivotal Cloud Foundry

#Lab Overview

In this lab activity you'll be using **Pivotal Cloud Foundry (PCF)** to deploy, scale and manage the application that you deployed in the previous Docker Lab


# Installing PCF Dev

Please perform PCF Dev Installation following these instructions:

[PCF Dev Basic Installation](https://my.syncplicity.com/share/2t7rvqo5igl9jd6/PCF%20Dev%20rev%200.3)

#Lab Overview

In this session you'll be less guided so please free to use and abuse Google searching capabilities ;)

This is what we would like you to achieve:
* Get sample app from git
* Push it to PCF dev
* Examine its logs
* Scale the Application
* Change the application and redeploy it
* BONUS: BLUE/GREEN Deployment

#Example Application

Here is the application available for you to deploy and edit:

https://github.com/dotnext/cf-sample-app

The Application has multiple endpoints:

* `/`: Display a title, index number for the app, and uptime for the running instance.
* `/env`: Display a nicely formatted output of the environment variables
* `/port`: Return the port number the application is listening on
* `/exit`: Displays a warning message and then forcibly exits the server, (hopefully) causing CF to restart the instance

#Application Details

Here is how the app should loook like when deployed:

`/` endpoint:

![index](https://raw.githubusercontent.com/dotnext/cf-sample-app/master/images/index.png)

`/env` endpoint:

![env](https://raw.githubusercontent.com/dotnext/cf-sample-app/master/images/env.png)


#Bonus Stage

Deploy the Application on PCF but using Docker Containers

**HINT:** You have some instructions in the PCF dev installation document ;)
