# Table of Contents

0. [Chapter 0 : Plugins](#chapter-0)
1. [Chapter 1 : Key CI/CD/Jenkins Concepts](#chapter-1)
2. [Chapter 2 : Jenkins usage (features and functionality)](#chapter-2)
3. [Chapter 3 : Building Continuous Delivery (CD) Pipelines](#chapter-3)
3. [Chapter 4 : CD-as-Code Best Practices](#chapter-4)

<a name="chapter-0"></a>
Chapter 0 : Plugins 
===================
Amazon EC2 Plugin
-----------------
Allow Jenkins to start slaves on EC2 or Eucalyptus on demand, and kill them as they get unused.With this plugin, if Jenkins notices that your build cluster is overloaded, it'll start instances using the EC2 API and automatically connect them as Jenkins slaves. When the load goes down, excessive EC2 instances will be terminated. This set up allows you to maintain a small in-house cluster, then spill the spiky build/test loads into EC2 or another EC2 compatible cloud.
* https://wiki.jenkins-ci.org/display/JENKINS/Amazon+EC2+Plugin

Build Pipeline Plugin
---------------------
This plugin provides a Build Pipeline View of upstream and downstream connected jobs that typically form a build pipeline.  In addition, it offers the ability to define manual triggers for jobs that require intervention prior to execution, e.g. an approval process outside of Jenkins.
* https://wiki.jenkins-ci.org/display/JENKINS/Build+Pipeline+Plugin 

CloudBees Docker Build and Publish Plugin
-----------------------------------------
This plugin provides the ability to build projects with a Dockerfile, and publish the resultant tagged image (repo) to the docker registry.
* https://wiki.jenkins-ci.org/display/JENKINS/CloudBees+Docker+Build+and+Publish+plugin
* https://github.com/jenkinsci/docker-build-publish-plugin/blob/master/README.md

CloudBees Folders Plugin
------------------------
This plugin allows users to create "folders" to organize jobs. Users can define custom taxonomies (like by project type, organization type etc). Folders are nestable and you can define views within folders.
* https://wiki.jenkins-ci.org/display/JENKINS/CloudBees+Folders+Plugin

Copy Artifact Plugin
--------------------
Adds a build step to copy artifacts from another project. The plugin lets you specify which build to copy artifacts from (e.g. the last successful/stable build, by build number, or by a build parameter). You can also control the copying process by filtering the files being copied, specifying a destination directory within the target project, etc. Click the help icon on each field to learn the details, such as selecting Maven or multiconfiguration projects or using build parameters. You can also copy from the workspace of the latest completed build of the source project, instead of its artifacts. All artifacts copied are automatically fingerprinted for you.
* https://wiki.jenkins-ci.org/display/JENKINS/Copy+Artifact+Plugin

Credentials Plugin
-----------------
This plugin allows you to store credentials in Jenkins.
The credentials plugin provides a standardized API for other plugins to store and retrieve different types of credentials. User visible features are:

A “Manage Credentials” screen on the “Manage Jenkins” screen allowing you to manage system and global credentials.
If you are using Jenkins security, when you go to “Users” / your username / “Configure” you would see the option to manage personal credentials.
Anywhere those credentials are needed, there is a drop down list of the appropriate available credentials, and you just select the appropriate one.
When the time comes to change the password, you just change it once. 
And that is about it, from the end-user's perspective. A single point for managing each credential. Change it in one place and you are done.

As of version 1.5, the plugin now supports categorising credentials into different "domains" in order to allow plugins to restrict the choice of credentials to only those that are appropriate.
* https://wiki.jenkins-ci.org/display/JENKINS/Credentials+Plugin

Delivery Pipeline Plugin
------------------------
Visualisation of Delivery/Build Pipelines, renders pipelines based on upstream/downstream jobs. Full screen view for information radiators.

In Continuous Delivery feedback and visualisation of the delivery process is one of the most important areas. When using Jenkins as a build server it is now possible with the Delivery Pipeline Plugin to visualise one or more Delivery Pipelines in the same view even in full screen.
* https://wiki.jenkins-ci.org/display/JENKINS/Delivery+Pipeline+Plugin

Disk Usage Plugin
-----------------
This plugin records disk usage.
Showing disk usage trend graph is optional - unselect the "Show disk usage trend graph" checkbox on the global configuration page ("Manage Jenkins" -> "System configuration") if you don't want to see the graph on the project page.
When you install this plugin, disk usage is calculated each 60 minutes. You can see project list with occupied disk space by going to the "Disk Usage" page in the management section (Dashboard -> "Manage Jenkins" -> "Disk Usage"). The same page also allows you to schedule disk usage calculation immediately.
* https://wiki.jenkins-ci.org/display/JENKINS/Disk+Usage+Plugin

Docker Plugin
-------------
This plugin allows slaves to be dynamically provisioned using Docker.
The aim of the docker plugin is to be able to use a docker host to dynamically provision a slave, run a single build, then tear-down that slave.

Optionally, the container can be committed, so that (for example) manual QA could be performed by the container being imported into a local docker provider, and run from there.
* https://wiki.jenkins-ci.org/display/JENKINS/Docker+Plugin

Email-ext Plugin
----------------
This plugin extends Jenkins built in email notification functionality by giving you more control.  It provides customization of 3 areas.

Triggers - Select the conditions that should cause an email notification to be sent.
Content - Specify the content of each triggered email's subject and body.  
Recipients - Specify who should receive an email when it is triggered.
* https://wiki.jenkins-ci.org/display/JENKINS/Email-ext+plugin

Fingerprint Plugin
------------------
Adds the ability to generate fingerprints as build steps instead of waiting for a build to complete.
This is useful when the files used to create the fingerprint are generated before the end of the build since the owner of a fingerprint is based on the file age. It is also useful when using a plugin such as Join where you can call other jobs within the build steps. By generating the fingerprints prior calling the other jobs, the upstream build will really be the owner of the fingerprint.
* https://wiki.jenkins-ci.org/display/JENKINS/Fingerprint+Plugin

Git Plugin
----------
This plugin allows use of Git as a build SCM, including repository browsers for several providers. A recent Git runtime is required (1.7.9 minimum, 1.8.x recommended). Interaction with the Git runtime is performed by the use of the Git Client Plugin, which is only tested on official git client. 
* https://wiki.jenkins-ci.org/display/JENKINS/Git+Plugin

Mailer Plugin
-------------
This plugin allows you to configure email notifications for build results. This is a break-out of the original core based email component.
* https://wiki.jenkins-ci.org/display/JENKINS/Mailer

IRC Plugin
----------
This plugin enables Jenkins to send build notífications via IRC and lets you interact with Jenkins via an IRC bot. Note that you also need to install the instant-messaging plugin
* https://wiki.jenkins-ci.org/display/JENKINS/IRC+Plugin

JUnit Plugin
------------
Allows JUnit-format test results to be published.
The JUnit plugin provides a publisher that consumes XML test reports generated during the builds and provides some graphical visualization of the historical test results (see JUnit graph for a sample) as well as a web UI for viewing test reports, tracking failures, and so on. Jenkins understands the JUnit test report XML format (which is also used by TestNG). When this option is configured, Jenkins can provide useful information about test results, such as trends.

This functionality was part of the Jenkins Core until it was split out to this plugin in version in 1.577.
* https://wiki.jenkins-ci.org/display/JENKINS/JUnit+Plugin

Jabber Plugin
-------------
Integrates Jenkins with the Jabber/XMPP instant messaging protocol. Note that you also need to install the instant-messaging plugin.
This plugin enables Jenkins to send build notifications via Jabber, as well as let users talk to Jenkins via a 'bot' to run commands, query build status etc.. 
* https://wiki.jenkins-ci.org/display/JENKINS/Jabber+Plugin

Matrix Project Plugin
---------------------
Multi-configuration (matrix) project type.
A multi-configuration project is useful for instances where your builds will make many similar build steps, and you would otherwise be duplicating steps.
The Configuration Matrix allows you to specify what steps to duplicate, and create a multiple-axis graph of the type of builds to create.
* https://wiki.jenkins-ci.org/display/JENKINS/Matrix+Project+Plugin
* https://wiki.jenkins-ci.org/display/JENKINS/Building+a+matrix+project

NodeLabel Parameter Plugin
--------------------------
This plugin adds two new parameter types to job configuration - node and label, this allows to dynamically select the node where a job/project should be executed.
* https://wiki.jenkins-ci.org/display/JENKINS/NodeLabel+Parameter+Plugin

Parameterized Trigger Plugin
----------------------------
This plugin lets you trigger new builds when your build has completed, with various ways of specifying parameters for the new build.
You can add multiple configurations: each has a list of projects to trigger, a condition for when to trigger them (based on the result of the current build), and a parameters section.

There is also a ﻿Parameterized Remote Trigger Plugin in case you want to trigger a build on a different/remote Jenkins Master.
* https://wiki.jenkins-ci.org/display/JENKINS/Parameterized+Trigger+Plugin

Pipeline Plugin (formerly known as Workflow)
--------------------------------------------
A suite of plugins that lets you orchestrate automation, simple or complex.
The default interaction model with Jenkins, historically, has been very web UI driven, requiring users to manually create jobs, then manually fill in the details through a web browser. This requires additional effort to create and manage jobs to test and build multiple projects, it also keeps the configuration of a job to build/test/deploy separate from the actual code being built/tested/deployed. This prevents users from applying their existing CI/CD best practices to the job configurations themselves.
* https://wiki.jenkins-ci.org/display/JENKINS/Pipeline+Plugin
* https://jenkins.io/solutions/pipeline/

Promoted Builds Plugin
----------------------
This plugin allows you to distinguish good builds from bad builds by introducing the notion of 'promotion'.Put simply, a promoted build is a successful build that passed additional criteria (such as more comprehensive tests that are set up as downstream jobs.) The typical situation in which you use promotion is where you have multiple 'test' jobs hooked up as downstream jobs of a 'build' job. You'll then configure the build job so that the build gets promoted when all the test jobs passed successfully. This allows you to keep the build job run fast (so that developers get faster feedback when a build fails), and you can still distinguish builds that are good from builds that compiled but had runtime problems.

Another variation of this usage is to manually promote builds (based on instinct or something else that runs outside Jenkins.) Promoted builds will get a star in the build history view, and it can be then picked up by other teams, deployed to the staging area, etc., as those builds have passed additional quality criteria. In more complicated scenarios, one can set up multiple levels of promotions. This fits nicely in an environment where there are multiple stages of testings (for example, QA testing, acceptance testing, staging, and production.)
* https://wiki.jenkins-ci.org/display/JENKINS/Promoted+Builds+Plugin

Radiator View Plugin
--------------------
Provides a job view displaying project status in a highly visible manner. This is ideal for displaying on a screen on the office wall as a form of Extreme Feedback Device.
 
Once the plugin is installed, click on the add view tab and select "Radiator View". The job selection options are the same as the standard list view -- either select projects to include or specify a regular expression to select the options. 
This plugin will be integrated with the claim plugin if it is installed - claimed failures are displayed in a column on the right. 
* https://wiki.jenkins-ci.org/display/JENKINS/Radiator+View+Plugin

SMS Notification Plugin
-----------------------
This is Jenkins plugin that sends SMS notification whenever there's a failed build. The plugin is powered by Hoiio API

Hoiio API is set of telephony API that integrate telephony services - phone calls, conference, IVR (Interactive Voice Responses), Fax and SMS - into your services and website easily.
* https://wiki.jenkins-ci.org/display/JENKINS/SMS+Notification

Script Security Plugin
----------------------
Various Jenkins plugins require that users define custom scripts, most commonly in the Groovy language, to customize Jenkins’s behavior. If everyone who writes these scripts is a Jenkins administrator—specifically if they have the Overall/RunScripts permission, used for example by the Script Console link—then they can write whatever scripts they like. These scripts may directly refer to internal Jenkins objects using the same API offered to plugins. Such users must be completely trusted, as they can do anything to Jenkins (even changing its security settings or running shell commands on the server).

However, if some script authors are “regular users” with only more limited permissions, such as Job/Configure, it is inappropriate to let them run arbitrary scripts. To support such a division of roles, the Script Security library plugin can be integrated into various feature plugins. It supports two related systems: script approval, and Groovy sandboxing.
* https://wiki.jenkins-ci.org/display/JENKINS/Script+Security+Plugin

Skype Plugin
------------
Integrates Jenkins with Skype for instant messaging. Requires extra manual installation steps!!!
Note that you also need to install the instant-messaging plugin.

This plugin enables Jenkins to send build notifications via Skype, and to talk to Jenkins via a 'bot' to run commands, query build status etc.. 
* https://wiki.jenkins-ci.org/display/JENKINS/Skype+Plugin


<a name="chapter-1"></a>
Chapter 1 : Key CI/CD/Jenkins Concepts 
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

|         | Definition    |
| ------------- |:-------------:|
| continuous integration     | TODO |
| continuous delivery     | TODO      |
| continuous deployment | TODO    |


### Difference between CI and CD
TODO

### Stages of CI and CD
TODO

### Continuous delivery versus continuous deployment
TODO

Jobs
----
### What are jobs in Jenkins?
TODO

### Types of jobs
TODO

### Scope of jobs
TODO

Builds
------
### What are builds in Jenkins?
TODO

### What are build steps, triggers, artifacts, and repositories?
TODO

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
|         | Definition    |
| ------------- |:-------------:|
| unit test    | TODO |
| smoke test    | TODO      |
| acceptance test | TODO    |
|automated verification/functional tests | TODO |

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
### What are fingerprints?
TODO

### How do fingerprints work?
TODO

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

<a name="chapter-2"></a>
Chapter 2 : Jenkins usage (features and functionality)
======================================================
Resources
---------
* https://wiki.jenkins-ci.org/display/JENKINS/Distributed+builds#Distributedbuilds-Schedulingstrategy
* https://wiki.jenkins-ci.org/display/JENKINS/Post-initialization+script
* https://wiki.jenkins-ci.org/display/JENKINS/Features+controlled+by+system+properties
* https://www.cloudbees.com/blog/parallelism-and-distributed-builds-jenkins

Jobs
----
### Organizing jobs in Jenkins
TODO

### Parameterized jobs
TODO

### Usage of Freestyle/Pipeline/Matrix/Maven/Literate
TODO


Builds
------
### Setting up build steps and triggers
TODO

### Configuring build tools
TODO

### Running scripts as part of build steps
TODO


Source Code Management
----------------------
### Polling source code management
TODO

### Creating hooks
TODO

### Including version control tags and version information
TODO


Testing
-------
### Testing for code coverage
TODO

### Test reports in Jenkins
TODO

### Displaying test results
TODO

### Integrating with test automation tools
TODO

### Breaking builds

Notifications
-------------
### Setup and usage
TODO

### Email notifications, instant messaging, build radiators
TODO

### Alarming on notifications
TODO


Distributed Builds
------------------
### Setting up and running builds in parallel
TODO

### Setting up and using SSH agents, JNLP agents, cloud agents
TODO

### Monitoring nodes
TODO


Plugins
-------
### Setting up and using Plugin Manager
TODO

### Finding and configuring required plugins
TODO


CI/CD
-----
### Using Pipeline (formerly known as Workflow)
TODO

### Integrating automated deployment
TODO

### Release management process
TODO

### Pipeline stage behavior
TODO


Jenkins Rest API
----------------
### Using REST API to trigger jobs remotely, access job status, create/delete jobs
TODO


Security
--------
### Setting up and using security realms
TODO

### User database, project security, Matrix security
TODO

### Setting up and using auditing
TODO

### Setting up and using credentials
TODO


Fingerprints
------------
### Fingerprinting jobs shared or copied between jobs
TODO


Artifacts
---------
### Copying artifacts
TODO

### Using artifacts in Jenkins
TODO

### Artifact retention policy
TODO


Alerts
------
### Making basic updates to jobs and build scripts
TODO

### Troubleshooting specific problems from build and test failure alerts
TODO

<a name="chapter-3"></a>
Chapter 3 : Building Continuous Delivery (CD) Pipelines
=======================================================
Resources
---------
* https://cloudbees.zendesk.com/hc/en-us/articles/203802500-Injecting-Secrets-into-Jenkins-Build-Jobs
* https://www.cloudbees.com/blog/credentials-api-jenkins
* http://documentation.cloudbees.com/docs/cje-user-guide/_list_views.html?query=view
* https://github.com/jenkinsci/jenkins/blob/3537831a42cd5b3b27a41fcde9b1f201962f38a1/core/src/main/grammar/crontab.g#L68-L71
* https://github.com/jenkinsci/jenkins/blob/3537831a42cd5b3b27a41fcde9b1f201962f38a1/core/src/main/resources/hudson/triggers/TimerTrigger/help-spec.html#L45-L46
* https://github.com/jenkinsci/workflow-plugin/blob/feb5bf44573dfc9379d9551f12b0372907e787be/README.md#pause-and-resume-execution
* https://github.com/jenkinsci/workflow-plugin/blob/feb5bf44573dfc9379d9551f12b0372907e787be/aggregator/src/test/java/org/jenkinsci/plugins/workflow/steps/ExecutorStepTest.java#L165-L214
* https://github.com/jenkinsci/workflow-plugin/blob/e0263fc7275e804785e4e93054ef0f2f2945a2dc/basic-steps/src/main/resources/org/jenkinsci/plugins/workflow/steps/WriteFileStep/help.html#L1
* https://wiki.jenkins-ci.org/display/JENKINS/Jenkins+CLI

Pipeline Concepts
-----------------
### Value stream mapping for CD pipelines
TODO

### Why create a pipeline?
TODO

### Gates within a CD pipeline
TODO

### How to protect centralized pipelines when multiple groups use same tools
TODO

### Definition of binary reuse, automated deployment, multiple environments
TODO

### Elements of your ideal CI/CD pipeline - tools
TODO

### Key concepts in building scripts (including security/password, environment information, etc.)
TODO


Upstreams and downstreams
-------------------------
### Triggering jobs from other jobs
TODO

### Setting up the Parameterized Trigger plugin
TODO

### Upstream/downstream jobs
TODO


Triggering
----------
### Triggering Jenkins on code changes
TODO

### Difference between push and pull
TODO

### When to use push vs pull
TODO


Pipeline (formerly known as Workflow)
-------------------------------------
### Benefits of Pipeline vs linked jobs
TODO

### Functionalities offered by Pipeline
TODO

### How to use Pipeline
TODO

### Pipeline stage concurrency
TODO


Visualization
-------------
### Options to visualize jobs’ relationships
TODO

### When to use various options for visualizing jobs’ relationships
TODO

### Information offered by a build pipeline view
TODO

### How to set up build pipeline visualization
TODO


Folders
-------
### How to control access to items in Jenkins with folders
TODO

### Referencing jobs in folders
TODO


Parameters
----------
### Setting up test automation in Jenkins against an uploaded executable
TODO

### Passing parameters between jobs
TODO

### Identifying parameters and how to use them: file parameter, string parameter
TODO

### Jenkins CLI parameters
TODO


Promotions
----------
### Promotion of a job
TODO

### Why promote jobs?
TODO

### How to use the Promoted Builds plugin
TODO


CD Metrics
----------
### KPIs/metrics for CI/CD
TODO

### Determining how many builds failed, succeeded
TODO

### Determining how long a build takes
TODO

### Determining how often code is checked-in
TODO

### How to use metrics/KPIs
TODO


Notifications
-------------
### How to radiate information on CD pipelines to teams
TODO

<a name="chapter-4"></a>
Chapter 4 : CD-as-Code Best Practices
=====================================
Resources
---------
* http://documentation.cloudbees.com/docs/cookbook/_distributed_builds_architecture.html
* http://documentation.cloudbees.com/docs/cookbook/_distributed_builds_architecture.html
* http://documentation.cloudbees.com/docs/cookbook/_choosing_the_right_hardware_for_masters.html
* http://documentation.cloudbees.com/docs/cookbook/_architecting_for_scale.html
* http://documentation.cloudbees.com/docs/cookbook/_containers.html
* http://documentation.cloudbees.com/docs/cookbook/pipeline-as-code.html
* http://documentation.cloudbees.com/docs/cookbook/_setting_up_high_availability_with_cloudbees_high_availability_plugin.html
* https://wiki.jenkins-ci.org/display/JENKINS/Remoting+issue

Distributed builds architecture
-------------------------------
TODO

Fungible (replaceable) agents
-----------------------------
TODO

Master-agent connectors and protocol
------------------------------------
TODO

Tool installations on agents
----------------------------
TODO

Cloud agents
------------
TODO

Containerization
----------------
TODO

Traceability
------------
TODO

High availability
-----------------
TODO

Automatic repository builds
---------------------------
TODO
