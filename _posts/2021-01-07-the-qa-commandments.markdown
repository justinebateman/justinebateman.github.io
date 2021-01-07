---
title:  "The QA Commandments"
date:   2021-01-07 16:08:32 +0000
categories:
  - Blog
excerpt: Don’t test only what the story tells you to, Don’t forget about user experience, Don’t let developers bias you, Don’t write bad bug reports
toc: true
tags:
  - testing
  - process
  - strategy
  - qa
---

### Don’t test only what the story tells you to

User stories often have acceptance criteria added by a product owner or business analyst. These are usually helpful for QA to know when they can consider a story as “Passed QA”. However, it’s important not to just stick to the AC and test only the “Happy Path” for a feature. The AC usually tells us what we want to happen, but it’s our job as testers to think about what could happen. Remember to use your QA skills to think outside the box and run validation and negative tests to improve your test coverage on a story.

### Don’t forget about user experience

Sometimes when we’re working to a deadline and have a lot of QA tasks we get so focused on just the functionality of a feature. If we can’t find any bugs and the tests pass then we move the ticket to the “Passed” column, and move on to next thing on the list. When this happens, we often miss user experience issues because we “can’t see the wood for the trees”. A feature might work as designed, and with no functional defects but it might be really painful and frustrating to use. Usability issues can result in loss of users just as much as a functional defect can. Remember to put yourself in the shoes of the end user when you’re testing, and if a behaviour would frustrate you, recommend changing it.  


### Don’t let developers bias you

Sometimes, with a complicated user story a developer may meet with the QA team to do a demo of the feature they’ve developed. This can aid understanding in the scope of what needs tested, and any risk areas. However, it can also result in the opposite effect where testers are biased by the developers into assuming something will work. A dev may demo a particular section of a feature and casually mention “I tested this really well and it all works great”. We might then gloss over thoroughly testing this section, and miss an important defect. The developer is already biased because they created the feature, and they’re confident everything works before they hand it over for testing. A testers motto should be “Everything is guilty until proven innocent.” Just because a developer is confident that something will work perfectly in production doesn’t mean we should be until we’ve seen it for ourselves in a variety of scenarios. 

### Don’t write bad bug reports

If a bug report is effective then the chances of having the issue fixed are higher, we’ve all had bugs rejected because the developer can’t reproduce it. 

Ensure you have a clear, unambiguous, step by step guide to reproduce the issue. Putting these steps in a bullet point or numbered list makes it more difficult for a step to be missed. A screenshot of the issue is always useful, a screen recording of the steps is often even better. Some good tools for screen recording are: [ShareX on Windows](https://getsharex.com/) or [LICEcap on macOS](https://www.cockos.com/licecap/)

Be specific with your report, don’t write an essay about what’s wrong, keep it to the point. Be careful also not to combine multiple problems even if they seem similar in nature. Compartmentalise your thinking and separate the issues into separate tickets so they can be addressed and retested separately. 

Include as much relevant information as you can to make it quicker and easier for the developer to diagnose the problem. If the issue is only occurring in one browser – state that. If there are errors in the browser console log, copy and paste the full log into the bug report. If your application makes use of a logging tool like Splunk, check the logs for anything relevant and include these in your report. 
