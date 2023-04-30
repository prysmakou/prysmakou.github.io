---
layout: post
title:  "2023 Week 16 Week Retro"
date:   2023-04-23 09:17:19 +0100
categories: update
---
# What I'm up to

- Kubernetes (EKS) clusters maintenance
AWS folks published new version of ALB Ingress Controller.
Among other changes there are a couple of long-awaited:
* Remove constraints of multiple TLS on certificate auto-discovery
  The presence of more than one certificate for a domain in a region is not an issue anymore! (the most frequent error so far)
* Validate Ingress condition annotations
Earlier if at least 1 ingress in the group has an invalid annotation the rest of the ingresses in the group aren't took into account during building listener rules.
The condition validation errors handled separately to prevent the termination of the process of the building listener rules for valid ingresses if such an error occurs.
- AWS Accounts Management
Accounts migration (to another AWS organisation) requires planning, testing and a good runbook.  

