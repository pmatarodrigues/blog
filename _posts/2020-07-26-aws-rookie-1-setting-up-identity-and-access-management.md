---
draft: false
layout: post
title: 'AWS Rookie #1 - Setting up Identity and Access Management'
description: This is the start of my journey through AWS and I'll try to describe all of the things that helped me on this path. All the good resources, cool people and tools will be featured here
summary: This is the start of my journey through AWS and I'll try to describe all of the things that helped me on this path. All the good resources, cool people and tools will be featured here.
tags: cloud
minute: 2
date: 2020-07-26T01:28:20.170Z
---

You know when you just get tired of everything else you've been working on the last few years and decide to start fresh?

**That's not what happened to me**.

I still love what I do and I'll keep working on my side projects and learning new languages and everything. It's just that I've been reading a lot about the **cloud** **architecture** and I'm starting to feel like I need to invest in this.

So, this is it. This is the start of my journey through **AWS** and I'll try to describe all of the things that helped me on this path. All the **good resources**, **cool people** and **tools** will be featured here. Wish me luck \\o/

![](https://media.giphy.com/media/RrVzUOXldFe8M/giphy.gif)

## IAM - Identity and Access Management

The Identity and Access Management (IAM) is a AWS service that enables you to manage the access to your AWS services and resources.

With IAM you can control who has access to your AWS account, what type of access they have to what service and what actions can be executed.

There's a set of keywords that are crucial to understanding this service, as described below:

* [User](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users.html) - Normally is created to represent a person or application can interact with AWS.
* [Group](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups.html) - Is a collection of Users. Groups let you specify permissions for multiple users, which can make it easier to manage their permissions.
* [Role](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) - Almost like a User. You can use roles to give access to users, applications, or services that don't normally have access to your AWS resources.
* [Permission](https://aws.amazon.com/iam/features/manage-permissions/) - Permissions let you establish access to AWS resources to IAM entities (users, groups, and roles). Without your permissions, entities can't use anything on your AWS.
* [Policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html) - A policy defines the permissions are associated with some identity or resource. Policies consist of three attributes that define what type of access you have:
  * Effect - Allow or Deny permission
  * Action - API calls that can be made
  * Resource - Scope of entities that the policy rule covers

---

## Best Practices

#### Lock your account root user and create individual IAM users

The root account access key gives full access to all the services and billing information, therefore root access should be handled very carefully.

#### Enable multi-factor authentication for all users

MFA grants you another layer of protection. If some user's access is compromised, there's still another layer of security to be broken by some kind of attacker.

#### Grant least privilege to users and resources

Give your users and resources only the necessary permissions to perform the specific task that they'll be working on.

#### Configure a strong password policy for your users

Everyone should avoid "password" and "123456" passwords. Make your users choose strong ones, with numbers and special characters with minimum number of characters.

#### Monitor activity in your AWS account and Remove unnecessary credentials

Monitoring your AWS logs can be useful to check the date and time of each users' actions, and therefore review their permissions and remove credentials that aren't related to them.

#### Setup CloudTrail

CloudTrail creates a "trail" of events for actions taken by a user, role, or an AWS service.

#### Don't commit credentials to git

This one is just common sense actually.

***

IAM may seem a really basic tool when you start using it, but as the complexity of your systems increases, so does the amount of attention you have to give to IAM.

Hope you enjoyed this first chapter, stay tuned for more! ;D


### Cool Resources

* [https://aws.amazon.com/blogs/security/](https://aws.amazon.com/blogs/security/ "https://aws.amazon.com/blogs/security/")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html")
* [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html "https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html")
* [https://iam.cloudonaut.io/](https://iam.cloudonaut.io/ "https://iam.cloudonaut.io/")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html")
* [https://aws.amazon.com/iam/features/mfa/?audit=2019q1](https://aws.amazon.com/iam/features/mfa/?audit=2019q1 "https://aws.amazon.com/iam/features/mfa/?audit=2019q1")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html")
* [https://start.jcolemorrison.com/aws-iam-policies-in-a-nutshell/](https://start.jcolemorrison.com/aws-iam-policies-in-a-nutshell/ "https://start.jcolemorrison.com/aws-iam-policies-in-a-nutshell/")
* [https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html "https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html")