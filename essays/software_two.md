---
layout: essay
type: essay
title: "Software Engineering (Part II)"
# All dates must be YYYY-MM-DD format!
date: 2025-05-16
published: true
labels:
  - Software Engineering
  - ICS 414
---

<p align="center">
  <img src="../img/software-two/teamwork.png" width="450px">
</p>

## First Reaction

After I enjoyed the teamwork experience of the ICS 314 course, I had thought that I should practice software engineering further through ICS 414: Software Engineering II. But from the first day of class, I could tell that there is a fundamental difference between teams: the lack of **team bonding**. The ICS 414 course assumes basic mastery over fundamental software development skills by blindly assigning each student to a team of eight members, which almost doubles the expected four-person team from ICS 314. Software Engineering II advertises challenge through this random assignment of manpower, and through the adversity of excess personnel.

My personal grievance against this agenda is the lack of team bonding. In ICS 314, a student will bond with classmates seated nearby over the course of the semester. It is near the end of the semester when the final project is assigned, and students will need to seek out teammates. It is at this point that students would be more confident in developing a bigger project as a team. On the other hand, ICS 414 lacks this sense of familiarity among students. This primarily hurts teams that consist of reserved students. Communication becomes particularly crucial when more people are involved on a project, but the lack of prior bonding deters students from consistently communicating with the team. Even given the benefit of doubt, I had personally become discouraged by talking to a wall.. figuratively speaking.

## Valuable Lessons

Personal feelings aside, ICS 414 builds on top of the foundations of ICS 314 but with more room for freedom *(though at the mercy of our client)*. Drawing from ICS 314, groups made use of the same minimal technology stack: Typescript, git, markdown, VSCode IDE, GitHub, ESLint, HTML, CSS, Bootstrap 5, React, PostgreSQL, Prisma ORM, Nextjs, and Vercel. As one example of the liberty given by the client project, my group had forgo Bootstrap 5 in favor of Tailwind CSS. The only strict requirements by our client were the implementation of different users with distinct permissions, and to seamlessly integrate excel spreadsheets containing financial data into a web-based application. 

During development, I had found that the lack of consistent communication between the team led to many errors pushed to the main branch. To adhere to coding standards, we utilized ESLint to help improve our code quality. This had slightly backfired, as late night pushes led to most of our errors resulting from ESLint. As a compromise, our group utilized a rule preventing direct merges to the main branch without review by someone else in our team. This rule also prevented pushes that contained errors. In the long run, this rule helped mitigate further debugging efforts but it was also a slight burden. Due to the lack of consistent communication between our team, I found myself to be the primary reviewer *(fair enough, I was the one to implement this rule)*, and code that I pushed would not be reviewed unless I were to find a teammate. In most cases, teammates would show up in the classroom but ICS 414 does not require in-person attendance as the semester drags on. Eventually, we agreed to drop this rule as less of us showed up in-person.

## Future Advice

For future ICS 414 students, my advice would be to work harder towards befriending teammates at the start. Solid team bonding activities would strengthen every team member’s motivation and willingness to communicate well. Also, although it may be daunting to develop a project for an actual client, I believe working effectively with one’s team to split up major project goals as microtasks would ease the stress of it. ICS 414 has taught me to not take a good team lightly. I cannot stress enough the importance of nurturing teamwork to be fulfilled by ICS 414. But this ideology is also relevant in professional environments, where individuals have no control over who their coworkers are.
