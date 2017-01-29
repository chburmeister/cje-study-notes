Module 1 : Key CI/CD/Jenkins Concepts 
======================================
Resources
---------
* http://www.martinfowler.com/articles/continuousIntegration.html
* http://martinfowler.com/bliki/ContinuousDelivery.html
* http://martinfowler.com/bliki/DeploymentPipeline.html
* http://www.informit.com/articles/article.aspx?p=1621865&seqNum=2
* http://devops.com/2014/07/29/continuous-delivery-pipeline/
* https://jaxenter.com/implementing-continuous-delivery-117916.html
* http://www.infoq.com/articles/orch-pipelines-jenkins
* http://technologyconversations.com/2014/04/29/continuous-delivery-introduction-to-concepts-and-tools/
* https://en.wikipedia.org/wiki/Continuous_delivery
* https://en.wikipedia.org/wiki/Artifact_%28software_development%29
* https://en.wikipedia.org/wiki/Build_automation
* https://en.wikipedia.org/wiki/Distributed_version_control
* https://en.wikipedia.org/wiki/List_of_version_control_software
* https://en.wikipedia.org/wiki/Smoke_testing_(software)
* https://wiki.jenkins-ci.org/display/JENKINS/Administering+Jenkins
* https://wiki.jenkins-ci.org/display/JENKINS/Terminology
* http://jenkins-ci.org/content/extreme-feedback-lamp-switch-gear-style
* https://wiki.jenkins-ci.org/display/JENKINS/Distributed+builds#Distributedbuilds-Offlinestatusandretentionstrategy
* https://wiki.jenkins-ci.org/display/JENKINS/Remoting+issue
* https://wiki.jenkins-ci.org/display/JENKINS/Matrix-based+security
* https://wiki.jenkins-ci.org/display/JENKINS/Remote+access+API
* https://wiki.jenkins-ci.org/display/JENKINS/Securing+Jenkins
* https://wiki.jenkins-ci.org/display/JENKINS/Quick+and+Simple+Security
* http://docs.openstack.org/infra/jenkins-job-builder/triggers.html
* https://www.simple-talk.com/opinion/opinion-pieces/branching-and-merging-ten-pretty-good-practices/
* http://stackoverflow.com/questions/520064/what-is-unit-test-integration-test-smoke-test-regression-test
* https://www.cloudbees.com/jenkins/about/notifications
* http://searchsecurity.techtarget.com/definition/authentication-authorization-and-accounting

Continuous Delivery/Continuous Integration Concepts
---------------------------------------------------

|         			| Definition    |
| ----------------------------- |:-------------:|
| continuous integration     	| TODO 		|
| continuous delivery     	| TODO      	|
| continuous deployment 	| TODO    	|


### Difference between CI and CD
TODO

### Stages of CI and CD
The commit statg asserts that the system works at the technical level. It compiles, passes a suite of (primarily unit-level) automated tests, and runs code analysis

Automated acceptance test stages assert that the system works at the functional and nonfuctional level, that behaviorally it meets the needs of its users and the specifications of its customers.

Manual test stages assert that the system is usable and fulfills its requirements, detects any defects that have not been caught by the automated tests and verify that it provides value to its users. That might include exploratory testing environments, integration environments and user acceptence tests.

Release stage delivers the system to the users/customers. Either as packaged software or by deploying it into a production or staging environment, where staging environment is as identical as possible to the production environment.

Automated acceptance test stages assert that the system works at the functional and nonfunctional level,	that	behaviorally	it	meets	the	needs	of	its	users	and	the
specifications	of	the	customer.


### Continuous delivery versus continuous deployment
TODO

Jobs
----
### What are jobs in Jenkins?
Synonymous with project.
Projects are containers for executing buildsteps. It consists of the following elements:

* optional SCM, such as CVS or Subversion where your source code resides.
* optional triggers to control when Jenkins will perform builds.
* some sort of build script that performs the build (ant, maven, shell script, batch file, etc.) where the real work happens
* optional steps to collect information out of the build, such as archiving the artifacts and/or recording javadoc and test results.
* optional steps to notify other people/systems with the build result, such as sending e-mails, IMs, updating issue tracker, etc.

In Jenkins 2: A user-defined model of a continuous delivery pipeline.

### Types of jobs

* Freestyle job : Freestyle build jobs are general-purpose build jobs, which provides a maximum of flexibility.
* Maven job : The “maven2/3 project” is a build job specially adapted to Maven projects. Jenkins understands Maven pom files and project structures, and can use the information gleaned from the pom file to reduce the work you need to do to set up your project.
* Monitor an external job: The “Monitor an external job” build job lets you keep an eye on non-interactive processes, such as cron jobs.
* Multiconfiguration job: aka “matrix project”, lets you run the same build job in many different configurations. This powerful feature can be useful for testing an application in many different environments, with different databases, or even on different build machines
* Copy existing job: creates a job identical to the given one, but you have to change the name.


### Scope of jobs
TODO

Builds
------
### What are builds in Jenkins?
Result of a single execution of a Project.

### What are build steps, triggers, artifacts, and repositories?

* Steps: A single task; fundamentally steps tell Jenkins what to do inside of Project.
* Triggers: A criteria for triggering a new Build.
* Artifacts: An immutable file generated during a Build which is archived onto the Jenkins Master for later retrieval by users.
* Repositories: TODO: scm or mvn ?

### Build tools configuration
TODO


Source Code Management
----------------------
### What are source code management systems and how are they used?
TODO

### Cloud-based SCMs
TODO

### Jenkins changelogs
TODO

### Incremental updates v clean check out
TODO

### Checking in code
TODO

### Infrastructure-as-Code
TODO

### Branch and Merge Strategies
TODO

### Testing
TODO

### Benefits of testing with Jenkins
TODO

### Define unit test, smoke test, acceptance test, automated verification/functional tests
|         					| Definition    |
| ----------------------------------------------|:-------------:|
| unit test    					| TODO 		|
| smoke test    				| TODO      	|
| acceptance test 				| TODO    	|
| automated verification/functional tests 	| TODO 		|

Notifications
-------------
### Types of notifications in Jenkins
TODO

### Importance of notifications
TODO

Distributed Builds
------------------
### What are distributed builds?
TODO

### Functions of masters and agents
TODO

Plugins
-------
### What are plugins?
TODO

### What is the plugin manager?
TODO

Jenkins Rest API
----------------
### How to interact with it
TODO

### Why use it?
TODO

Security
--------
### Authentication versus authorization
TODO

### Matrix security
TODO

### Definition of auditing, credentials, and other key security concepts
TODO

Fingerprints
------------
* https://wiki.jenkins-ci.org/display/JENKINS/Fingerprint
### What are fingerprints?
The fingerprint of a file is simply a MD5 checksum. Jenkins maintains a database of md5sum, and for each md5sum, Jenkins records which builds of which projects used. This database is updated every time a build runs and files are fingerprinted.

To avoid the excessive disk usage, Jenkins does not store the actual file. Instead, it just stores md5sum and their usages. These files can be seen in $JENKINS_HOME/fingerprints

Plugins can store additional information in these records. For example, Deployment Notification Plugin tracks files deployed on servers via chef/puppet through fingerprints.

### How do fingerprints work?
When you have interdependent projects on Jenkins, it often becomes hard to keep track of which version of a file is used by which version of a dependency on that file. Jenkins supports file fingerprinting to track dependencies.

For example, suppose you have the TOP project that depends on the MIDDLE project, which in turn depends on the BOTTOM project. You are working on the BOTTOM project. The TOP team reported that bottom.jar that they are using causes an NPE, which you (a member of the BOTTOM team) thought you fixed in BOTTOM #32. Jenkins can tell you which MIDDLE builds and TOP builds are using (or not using) your bottom.jar #32.

Artifacts
---------
### How to use artifacts in Jenkins
TODO

### Storing artifacts
TODO

Configuration Management (Tools such as Chef, Puppet, etc.)
-----------------------------------------------------------
### Elements of software configuration management
TODO

### Importance of software configuration management
TODO

Using 3rd party tools
---------------------
### How to use 3rd party tools with Jenkins
TODO

