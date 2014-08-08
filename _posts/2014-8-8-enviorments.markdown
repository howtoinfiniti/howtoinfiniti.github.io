---
layout: default
title:  "Enviorments"
---

There are several environments that ensure that every deployment artifact can be tested and verified by different parties. Figure Environments and actors. shows an overview of the environments. Note that the flow is always from dev to qa, from qa to staging and from staging to production.

<span class="bg bg-danger">Important</span> Always adhere to this order of deployment. Never skip environments unless you have really good reasons. Otherwise you risk introducing changes that will make debugging and deployments very complicated.

<img src="/images/user_properties.png" alt="User properties" class="img-responsive">