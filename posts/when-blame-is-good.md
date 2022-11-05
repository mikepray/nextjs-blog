---
title: 'When Blame is Good'
date: '2022-11-5'
---

![Lake](/images/IMG_4976.png "Sailing at the Lake")


**The Blame Game**

*"Don't play the blame game - focus on solutions"*. I've heard this phrase spoken during troubled times in an organization. This is good practice - at the point in time where something bad has already happened (production outage, project failure, reorganization, etc), moving forward is better for morale than a vitriolic assignment of wrongdoing. Solving the proximate problem requires alignment. But like all fluffy organizational aphorisms, "don't play the blame game" tries to be flexible with reality and it obscures the axiom of causation: things happen for a reason.

After the servers are back up, it's time for a root cause analysis. What happened? What went wrong? Who screwed up? Blame becomes useful, but only when applied correctly. Imagine a scenario where an outage is caused by a junior developer's mistake, perhaps a code change was pushed to production that failed a test and prevented a node from starting up. Once this mistake is discovered to be the cause of the outage, senior engineers swoop in with righteous incredulity to berate the obvious failure of running tests locally before pushing code. The advice to the hapless junior dev is simple: remember to run tests and "get good". 

This *appears* to be the correct use of blame. The senior engineers were correct: the proximate cause of the outage was indeed the junior developer's mistake. But look beyond the surface and you might discover something wrong with this assignment. The junior developer is a junior for a reason. They were hired as a junior and should be provided the latitude to make mistakes (within reason). What else happened?

In this (hopefully relatable) imaginary strawman, what actually happened was:
- the lack of any kind of code review process 
- the pipeline doesn't check for failing unit tests
- infrastructure that could not start up with a failing test or roll back to a previous successful build
- a manager who approved the PR without any due diligence

Should the junior dev also be blamed for the above problems? A real root cause analysis would go farther than admonishing the junior dev to improve their mental checklist. It would discover that in fact the senior engineers should shoulder some blame for not recommending or implementing a more robust PR process. Further, the analysis would discover that the absentee manager is really at fault for failing to implement any kind of safety net, failing to take action on the insufficient infrastructure, and failing to take accountability for their team member's basic mistake.

Ultimately the blame should follow the critical path of accountability in an organization. In this scenario, a junior developer made a simple mistake, but the team's manager had the responsibility to put a system in place that would permit their junior developer to make mistakes without impacting production. The senior engineers bear some blame for failing to notice or take action on the systemic problems, to the extent that their job responsibilities entail technical ownership of the system.

To extend the strawman further, imagine that the team's manager is notorious for a lack of technical leadership. It turns out that this manager simply does not have the technical ability to understand the problems in the team's systems. The path of accountability therefore moves up a level to the director, and so on and so forth until ultimately the blame for even a single mistake is to some degree shouldered by the executive leadership of the company.

**Good Blame**

In this exercise, blame follows the critical path of accountability upwards to the people in the positions of power to do something about the systemic problems, instead of being shouldered by relatively powerless line employees. This is what I mean by "good blame". Real positive change in organizations can't happen when blame is assigned to powerless employees. Even if the junior dev got good, the underlying organizational pathologies will continue unaddressed and another production outage is inevitable.

A realistic understanding of the critical path of blame would indicate that the team should put in checks to their pipeline, fix their infrastructure, and put into place a code review process. The manager should find a way to delegate technical decisions to their team or bring in a staff engineer from elsewhere in the organization for help. The director might look for a position in the organization more suited to the manager's skillset. 

This scenario is contrived to demonstrate this idea of the critical path of accountability. Real organizations will have their unique pathologies and combinations of imperfect systems. Advocating for this change (especially if you are the junior developer) is difficult, but I've seen it work. The important thing is to help your team discern between good and bad blame.

**In Summary**

Blame is good when it works with the **critical path of accountability** in an organization. Blame is bad when people in powerless positions are assigned fault. Discerning the difference and uncovering the critical path of accountability is important in order to make real change in an organization.