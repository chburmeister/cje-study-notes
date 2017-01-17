# Table of Contents
1. [Chapter 1 : Key CI/CD/Jenkins Concepts](#chapter-1)
2. [Chapter 2 : Jenkins usage (features and functionality)](#chapter-2)
3. [Chapter 3 : Building Continuous Delivery (CD) Pipelines](#chapter-3)
3. [Chapter 4 : CD-as-Code Best Practices](#chapter-4)

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
