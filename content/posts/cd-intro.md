+++
title = "Continuous Delivery Introduction"
draft = true
date = "2017-04-03T20:09:27-04:00"
tags = [ "agile" ]
categories = [ "getting-started", "continuous-delivery", "continuous-integration", "agile" ]
+++

# Overview 

Continuous delivery along with continuous integration supports the key fundamentals of software development using the agile methodology.

<!--more-->

Continuous delivery is the ability to produce new software to the end user at any time. Although different from continuous deployment to always be deploying any new code, continuous allows for deploying at any time, which may be at business defined intervals.

## Related to the Agile Manifesto

From http://agilemanifesto.org, continuous delivery is the first principle of the agile manifesto being labeled as the "highest priority". 

> Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.

Very closely to that principle is deliverying working software in shorter timescales, which is enabled by the ability of continuous delivery. 

> Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.

Both above principles are addressed with the concept of continuous delivery. Although continuous delivery is typically imagined to be continuous deploying new software to a user, delivery only refers to allowing for a deployment to occur. Deploying new versions to a production environment may be gated for business reasons, but that version can be made available at any time. See also https://continuousdelivery.com/2010/08/continuous-delivery-vs-continuous-deployment/.

Hand in hand with continuous delivery, continuous integration helps ensure the software we are delivering to be consistent quality. The folowing agil manifesto principle is reinforced by continuous integration.

> Continuous attention to technical excellence and good design enhances agility.

Continuous integration can be broken down to being continually integrating your code with the main branches in the code base, other services that are depended upon, backing services like databases and queues, and many forms of testing. Testing should be done with unit testing, integration testing, stress testing, functional testing, etc. Software should be written with tests as first class citizens, where you use a test first approach.

## Sample development flow 

In an ideal development experience of software development with continuous integration, delivery:

1. Tests added, source code changes, pushed up to branch in version control
2. Build is initiated from the code push (i.e. a hook), tests are run with unit tests first
3. Artifacts saved, deployed to an initial dev environment
4. Further testing like integration testing environment by environment
5. Delivered to the user

## Tools

For simple setup of a project, there are ready to go hosted solutions that can get a developer up and going with parts of continuous delivery in little time and effort.

1. Travis-CI [travis-ci.org](https://travis-ci.org)
2. Codeship [codeship.com](https://codeship.com)
3. CircleCI [circleci.com](https://circleci.com)
4. Wercker [wercker.com](https://wercker.com)
5. Drone.io [drone.io](https://try.drone.io)
6. Shippable [shippable.com](https://www.shippable.com)

Other solutions are more tightly integrated into a particular platform, like where the code repositories are hosted or where the deployments are delivered.

1. Gitlab [gitlab.com](https://about.gitlab.com)
2. Bamboo by Atlassian [atlassian.com](https://www.atlassian.com/software/bamboo)
3. Domino Data Lab [dominodatalab.com](https://www.dominodatalab.com/) Data Science platform
4. Google Cloud Platform [cloud.google.com](https://cloud.google.com)
5. AWS Code Pipeline [AWS codepipeline](https://aws.amazon.com/codepipeline)

Then a couple to point out that are nice, complete solutions with good flexibility. 

1. Visual Studio Team Services [visualstudio.com](https://www.visualstudio.com/team-services/)
2. Jenkins [jenkins.io](https://jenkins.io/)

These are obviously not exhaustive lists. There are for more solutions and tools, but these are good starting points to learn how they work with your unique code bases and products.
