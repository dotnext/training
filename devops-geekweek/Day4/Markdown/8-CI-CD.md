# CI-CD and PCF (title to be updated)


---

# What You'll Learn

* An introduction to DevOps Constructs and Buzzwords
* Whats is a Continuous Integration
* What is Continuous Deployment
* PCF architecture
* PCF Components
* Value of PCF

---

#DevOps Definition

A **collaborative culture & philosophy** between technical teams, often **derived from modern software development methods**

---

# DevOps Constructs and Buzzwords

![](http://i.imgur.com/dkmWVb3.jpg)

---

#As seen on Twitter

![](http://i.imgur.com/8v1NdC6.jpg)

---

#Cloud Native Applications

“Applications that do not require resilient infrastructure”

![](http://i.imgur.com/Ktw0HUM.jpg)

---

#Microservices

Properties of a Microservice
* Small code base
* Easy to scale, deploy and throw away
* Autonomous
* Resilient

Benefits of a Microservices Architecture
* A highly resilient, scalable and resource efficient application
* Enables smaller development teams
* Teams free to use the right languages and tools for the job
* Rapid application development

![](http://i.imgur.com/2VpJetT.jpg)

---

#Microservices Needs

Microservices are great, but they require:
* rapid provisioning
* solid monitoring
* rapid deployment
* devops culture

---

# Continuous Integration

* The practice of merging development work with a Master/Trunk/Mainline branch constantly so to test changes
* Promote the code testing as often as possible to catch issues early
* Most of the work is done by automated tests via a unit test framework
* Typically there is a build server performing these tests, so developers can continue working while tests are being performed

---

#Continuous Delivery
* The continual delivery of code to an environment once the developer feels the code is ready to ship
* Be it either UAT, Staging or Production environments
* The idea is to be constantly deliverying code to a user base, whether it be QA or customers for continual review and inspection
* Merges Continuous Integration with automated deployment, test and release
* Doesn’t mean every change is deployed to production ASAP but ready to be deployed at any time

---

#Phases of Continuous Delivery (too much?)

* Unit Test
* Code Quality Analysis
* Deploy to Test Environment 
* Integration Test 
* Packaging and Archiving 
* Deploy to Preproduction Environment 
* Acceptance Test
* Deploy to Production Environment

---

#CI/CD Tools
* Jenkins (https://jenkins.io/)
* Travis CI (https://travis-ci.org/ )
* Buildbot ( http://buildbot.net/ )
* Strider ( http://stridercd.com/ )
* Go (http://www.go.cd/ )
* Integrity (http://integrity.github.io/ )
 

---

##Microservices Drive Requirements around Logs and Performance Monitoring

* 10s or even 100s of microservices means a huge number of logs to comb through for an event
* performance analytics become critical when you have thousands of users and interdependent services

---

# Logging

* log everything
* no really, everything
* `chargers.cfapps.io` logs ~73 MB/day

---

# Logging Rules

* app never concerns itself with routing or storage of its output stream
* usually write to `stdout`
* include deep information as to file, module, function, lineno
* include a correlation id with every message
* log in UTC
* log with appropriate level: `debug` vs. `info` vs. `critical`

---

# Logging Tools

* use language-native tools for logging
  * python `logging`
  * node `winston` or `bunyan`
  * ruby `yell` or `logging`
* configurable tools are better tools
* multiple output streams are better
* multiple logging levels are better

---

# Log Management Tools

* splunk (http://www.splunk.com)
* loggly (http://www.loggly.com)
* logstash (https://github.com/elasticsearch/logstash)
  * "ELK" stack - elasticsearch, logstash, kibana
* graylog2
* many others

---

# Logging Tips
* send all logs to `stdout` **and** logging system
* set alerts on messages of give `type` per `minute|hour|whatever`
* use correlation id to track a given transaction/request

---

#gah, enough text!  what's it look like?

---

![fill](http://i.imgur.com/F9MkT7k.jpg)


