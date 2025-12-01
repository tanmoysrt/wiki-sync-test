---
route: handbook/how-bench-deploy-works
allow_guest: 0
published: 1
---

### Introduction

Let's understand how the bench update works by creating one. Bob is a developer and a freelancer who 
has been using Frappe and ERPNext for the last 5 years. Bob creates a custom app on top of frappe framework 
for his clients according to their requirements and hosts their site on AWS or with the client’s preferred 
cloud provider. Recently he got to know about Frappe Cloud and immediately signed up to test it. 
Bob is already in love with the ease of bench deployments and how quickly it is done. But he wants to 
understand how it all works behind the scenes.

### Release Group

When Bob creates a bench on the dashboard the first doctype which gets created is called Release Group. 
A Release Group is like a skeleton which defines the bench attributes such as servers, apps to be installed, 
configurations, dependencies etc. The base dependencies such as python, node and bench versions and configs 
are predefined for all the benches but they can be changed from the desk.

![Awaiting Deploy](/private/files/Awaiting%20Deploy.png)

At this point, Bob has only created the bench structure but there is no bench ready for Bob to create a site on. 
Bob needs to deploy the bench to use it. 

![Deploy](/private/files/Deploy.png)

On Deploy multiple doctypes are touched to create a single bench. They are:

* Deploy Candidate
* Deploy
* Bench
* Deploy Candidate Difference

Let’s go through them all one by one.

### What does a Deploy Candidate do?

When deploying a bench, first and foremost a deploy candidate is created. A deploy candidate defines what update
is being deployed. It’s like a release note which tells you all the update since the previous deploy. But deploy 
candidate does more than that.

It has mainly two functions: Build and Deploy. Build function creates a build directory and respective app 
directory on the server. It also generates the necessary config files for the production setup like supervisord, 
redis, common site config etc. and also builds a docker image from the generated dockerfile of the deploy candidate 
and pushes it to the docker registry.

The deploy function creates a deploy record for the deploy candidate. 

![Build](/private/files/Build.png)

### Deploy

A Deploy record is just record of servers with respective bench name in child table. Which parallelly creates 
bench on each server with defined configurations and dependencies from the release group.

![Flow Chart](/private/files/Flow.png)

### Bench

Bench tells you which release group it belongs to, which deploy candidate was it deploy from and the docker image url.

![Single Bench](/private/files/Single.png)

Bob now sees a ready bench to create a site on. If its the new bench you can start creating sites on this bench. 
However if its not a first bench in the release group there is one more step followed. With each bench a deploy candidate 
difference is also created.

### Deploy Candidate Difference

A deploy candidate difference record defines what changes are introduced since the previous deploy.

Let’s say after deploying the bench, bob forgot to add one custom app on the bench. Nothing to worry about Bob can 
still add the app on the bench. However to see the app on the bench and to use it, bench needs to be deployed again. 
Each time there is an update on any one of the apps installed on the bench or a new app is added on the bench, it needs 
to be deployed. And the entire flow from creating a deploy candidate to bench is followed again. You can find all your 
benches in the versions tab on Dashboard. 

![Versions](/private/files/Versions.png)

Deploy Candidate difference record helps you update from one bench to another.

> On an average day, on Frappe Cloud, there are roughly 250 benches, around 157 deploy candidates, 150 deploys and 
> almost 340 deploy candidate difference records are created and whooping 1700+ site update agent jobs are triggered 
> on a SINGLE DAY.
