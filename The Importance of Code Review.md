The Importance of Code Review
=============================

Code review is a time to enforce coding standards, coding style, and spread knoweldge

Code review is a two-way street. It's up to the developer to create a history that the code reviewer can get through quickly, so making your Git history such that your reviewer can review it quickly is something that's on the onus of the developer. Code review is important because we need at least two eyes on any piece of code before it gets into master. That's two gates the code has to go through to make it into production. It helps us with stability. It also spreads the knowledge so that two people know that piece of code. QA review is the third gate so that it has seen three eyes before getting into production. If you bring that kind of knowledge into anywhere you work, just making sure things go through multiple gates before getting into production, you're on your way to making maintainable, stable code.

The three gates provides accountability. If something does fail, that's because three people made the mistake. Because we do it this way, it does give a level of accountability that the code is right when it gets into production.

In code review, there are two people, the developer and the code reviewer. The easier you can make it on the code reviewer to understand your code, the easier your code review will go. At the end of the day, it's all about empathy. To empathize with the person, being in their shoes, if you're going through your commit history and you don't understand the story you're trying to tell or you can't easily digest what you did in that commit, then you probably need to go back and rebase. At the end of the day, it's about empathy, just making sure if you were handed that code review, would you like it?
