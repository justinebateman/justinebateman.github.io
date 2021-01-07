---
title:  "How Not to do QA"
date:   2019-04-02 16:08:32 +0000
categories:
  - Blog
excerpt: QA is not involved in each stage, Focusing on Cost rather than Value, Sacrificing Quality for Speed
tags:
  - testing
  - process
  - strategy
  - qa
---
{% include toc %}

### QA is not involved in each stage

QA is often referred to as simply “Testing”. In reality, [testing is only one of the things](https://intersog.com/blog/tech-tips/qa-vs-testing/) that a good QA engineer brings to a team. QA stands for Quality Assurance - a QA engineer aims to ensure the quality of the development process and its results. 

A good SDLC process has QA involved at each stage, right from planning through to support and maintenance. Testers often bridge the gaps between technical developers, product owners or stakeholders, and the end user. Testers are uniquely placed to have the most overall knowledge of how a product works from a user perspective, and also understand the technical details of what’s going on behind the scenes to make it work that way.

QA engineers then have a clear overview of the entire SDLC process and can point out inefficiencies and gaps. It’s their job to not only improve the quality of the end product, but also the process that’s used to develop it. 

### Focusing on Cost rather than Value

The earlier an issue is found the less money it costs. Consider a high priority issue reported to the customer support team that affects a large amount of users. The time taken to triage, investigate, debug, resolve, test, redeploy, and communicate the fix to stakeholders vs. if the problem had been discovered in a QA environment. The turnaround time for a fix would be a lot smaller and involve less people than dealing with a Production issue. 

The severity of the issue also needs to be taken into account, companies have gone out of business due to manufacturing a poor quality product. This could be because they faced lawsuits, or simply because their reputation was irreversibly damaged with their target consumer. 

An extreme example of this is the [Therac-25](https://hackaday.com/2015/10/26/killed-by-a-machine-the-therac-25/), a radiation therapy machine that caused accidental radiation overdoses killing at least six patients. This was caused by poor software developed with no QA process.

### Sacrificing Quality for Speed

There is a common misconception that QA slows down development. Many project managers/scrum masters see QA as a blocker to getting tasks into the Done column. However, if you factor the QA team into the process at an earlier stage it can actually save time in the long run. 

One of the most important stages in the SDLC is Requirements Gathering. Mistakes made during this stage echo throughout the entire lifecycle and end up having an impact on the product that makes it into the live environment. QA engineers often know your application better than anyone else on the team, so having them involved in requirements gathering and scope setting enables them to point out which solutions will and won’t work, and to remind the team of areas in the application they might not have considered. 

Introducing non functional QA like performance and load testing to your process can have a tangible impact on your server and hosting costs. Less hardware is required to run your application if performance is optimised, and less storage space is needed if we avoid saving data we don’t actually use. 

We can also improve staffing costs by investing in QA. If we prioritise QA resources and catch issues early we don’t need to invest as many resources into a Support team because they won’t have as much to do! 
