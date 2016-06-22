---
layout: post
title:  "Scaling the mountain in application maintenance and support"
date:   2016-06-22 10:39:11 +0800
categories: post
---

### Background
 
Currently, my company is involved in a government project and is doing a number of things in parallel, namely application maintenance (also known as production support), application enhancement and facility maintenance.
 
To set the context, the government organisation is in charge of granting legal documents for foreigners. The application being built has to be integrated with various legacy systems within the agency itself and also with other agencies. This increases the complexity of the system as we need to ensure that our data is kept in sync with the different legacy systems.
 
After the first feature went live, production support started immediately. The team handles tasks such as log monitoring, investigation of incidents, defect management and data patches. Timely response to incidents is important because an end user may be detained by the relevant authorities if any data is not in order.
 
### Incorporating log monitoring as part of the feedback cycle
 
We routinely monitor the system and application logs to ensure that everything is running smoothly. At times, we encounter exceptions which require an investigation to understand the root cause of the issue and come up with the necessary fix. Sometimes, through these investigations, scenarios and issues which previously went unnoticed are identified and highlighted. It is through such feedback cycles that we can improve the application, albeit the hard way.
 
### Making incidents  auditable and traceable
 
Because we are working with the government, every  incident needs to be auditable and traceable. In order to maintain a consistent standard, users raise issues through an email system maintained by a separate vendor while we also track them in Mingle. In the event where a service level agreement for the incident is breached, we will be fined by the government and therefore we need to resolve the issues in a timely fashion.
 
For every incident, it is important for us to record what happened and the impact to the users. After a thorough investigation, we state the analysis results and the proposed action like data patches or code fixes. Having proper documentation ensures that everything we do is auditable and traceable.
 
### Bridging gaps in an evolving application
 
While the application system continues to be refined, with more features being added, there are still functions which have yet to be built. Before we begin building these functions, multiple parties need to approve the change request and the funds take a long time to be received. Change takes time in the government.
 
As a stopgap, we perform data patches for functions which users are not able to perform through the application yet. There are a number of concerns while doing a data patch - is it legitimate, auditable, traceable? Over time, the team worked out a set of approval process which records the incident and the reason for data patch.  We built a small repeatable function that could be triggered from the pipeline. We also introduced procedures in the database that take snapshots of the data before and after the patch. These simple mechanisms make sure that a log trace is maintained for each action we perform to the application, for auditing purposes.
 
### Being honest is difficult but important
 
When we encounter issues in the production system, it is never easy to admit that something went wrong and we missed something along the way. However, honesty and transparency are crucial determinants to the speed and manner of resolving issues. Communicating what happened and why it happened is important because it allows the product owner and related parties to assess the impact and notify the affected parties. All parties can then come together as a team to focus on the issue and required solution. The key takeaway here is that honesty and transparency build trust which leads to more timely solutions.
 
### As a finishing note
 
This is the first time my company is engaged in a government project. We have learnt much through this involvement and we want to continue sharing these lessons.
 
To everyone who has been part of the journey, thank you.