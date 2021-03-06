---
title: "Serverless Framework Enterprise 0.10.0 - Deployment Profiles"
description: "With today’s Serverless Framework Enterprise release, we are extending the capabilities of Serverless Error Insights to support invocation logs access along with stack traces & more."
date: 2019-05-22
thumbnail: "https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/framework-enterprise-updates/deployment-profiles/serverless-enterprise-deployment-profiles-thumb.png"
heroImage: "https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/framework-enterprise-updates/deployment-profiles/serverless-enterprise-deployment-profiles-header.png"
category:
  - news
authors:
  - MaciejSkierkowski
---

With today’s Serverless Framework Enterprise release we are adding support for Deployment Profiles, enabling serverless development teams to move fast and scale while enforcing operational and security best practices. 

One of the greatest challenges of a scaling engineering team is educating new team members about organizational security and operational practices. This is especially challenging when those team members are also new to serverless. For example, when they deploy a service you want to make sure they deploy to the right regions and use the AWS Account designated for that stage. Or maybe you want to make sure that they do not deploy to production on Fridays.

Engineering Managers and Operators, with Serverless Framework Enterprise Deployment Profiles, can designate AWS Accounts for each of the stages in their applications, and enforce security and operational policies using Serverless Safeguards.

### AWS Accounts for each stage

AWS Credentials Access Role helps you secure your service deployments by enabling Serverless Framework Enterprise to issue temporary AWS Access Keys to deploy your services to AWS. The AWS Access Keys are generated by Serverless Enterprise on every command and the credentials expire after one hour. 

The AWS Credentials Access Roles are defined in the Deployment Profiles enabling your team to automatically use the right AWS Account for each stage.

<img src="https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/framework-enterprise-updates/deployment-profiles/serverless-enterprise-deployment-profile-creation.png">

### Safeguard Policies for each stage

Safeguards enable managers and operations teams to configure policies that must be complied with, like “restricted-deploy-times,” “required-stack-tags,” or “no-overly-generous-iam-role-statements,” in order for a Serverless Framework deployment to succeed. It comes with 15 safeguard policies available out of the box, with 9 pre-configure for you. If those policies aren’t enough, you can implement your own too.

Safeguards are configured in the Deployment Profiles enabling your team to comply with the requirements unique to each stage.

<img src="https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/framework-enterprise-updates/deployment-profiles/serverless-enterprise-safeguard.png">

### Safely deploy

By simply using Serverless Framework Enterprise, when you run `serverless deploy`, a short-lived AWS credentials will be generated and the Safeguard Policies will evaluated for that service before any resources are provisioned. With Deployment Profiles you can now automatically use the right AWS accounts and safeguard policies for each stage.

<img src="https://s3-us-west-2.amazonaws.com/assets.blog.serverless.com/framework-enterprise-updates/deployment-profiles/serverless-enterprise-safeguard-check.png">