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
