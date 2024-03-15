---
title : "Services"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 1.2 </b> "
---

## Services

A **service** within VPC Lattice is an independently deployable unit of software that delivers a specific task or function. 

A service can run on instances, containers, or as serverless functions within an account or a virtual private cloud (VPC). A service has a listener that uses rules, called listener rules, that you can configure to help route traffic to your targets. Targets can be EC2 instances, IP addresses, serverless Lambda functions, Application Load Balancers, or Kubernetes Pods. We can associate a service with multiple service networks

![Services](/images/1/0003-introduce.png?featherlight=false&width=50pc)
