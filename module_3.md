Module 3 : Building Continuous Delivery (CD) Pipelines
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

