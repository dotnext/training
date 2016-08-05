#Lab Docker Advanced

Welcome to your Docker Advanced Lab :)

In this session you'll be less guided so please free to use and abuse Google searching capabilities ;)


This is what we would like you to achieve:
* Get sample app from git
* write dockerfile
* compile image
* build swarm cluster
* push 2 containers to cluster
* edit app (just changing the html or adding some external microservice)
* compile
* redeploy your App again


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
