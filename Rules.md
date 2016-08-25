Merge small things faster.


Every commit should be compilable and unit testable.
====================================================

Types of Commits
================

 * Inject Dependency Commit
 * New Code Commit
 * Hookup Commit

 * Commits to highlight the discussion


Break formatting for clarity
============================

Never rewrite the history of your master, production branch
===========================================================

Feel free to rewrite the history of non-master branches, the branches not in production yet, but once they merge into master, don't look back. What's done is done.

OCD folks might want to make a history perfect, with no mistakes, but at some point you have to move on from the past. If it's in production, it's set in stone. Don't chisel away at Rock.


If two people on the team agree on a piece of code, let it into master.
=======================================================================

 * Central code reviewer
 * Code reviewer for certain parts of the system
 * System custodians
 * Code review is an essential part to merging 
 * Trust and empathy - It's all about empathy.

 * Code review is a time to enforce coding standards, coding style, and spread knoweldge

 * Code review is a two-way street. It's up to the developer to create a history that the code reviewer can get through quickly, so making your Git history such that your reviewer can review it quickly is something that's on the onus of the developer. Code review is important because we need at least two eyes on any piece of code before it gets into master. That's two gates the code has to go through to make it into production. It helps us with stability. It also spreads the knowledge so that two people know that piece of code. QA review is the third gate so that it has seen three eyes before getting into production. If you bring that kind of knowledge into anywhere you work, just making sure things go through multiple gates before getting into production, you're on your way to making maintainable, stable code.

 * The three gates provides accountability. If something does fail, that's because three people made the mistake. Because we do it this way, it does give a level of accountability that the code is right when it gets into production.

 * In code review, there are two people, the developer and the code reviewer. The easier you can make it on the code reviewer to understand your code, the easier your code review will go. At the end of the day, it's all about empathy. To empathize with the person, being in their shoes, if you're going through your commit history and you don't understand the story you're trying to tell or you can't easily digest what you did in that commit, then you probably need to go back and rebase. At the end of the day, it's about empathy, just making sure if you were handed that code review, would you like it?

 * Code bombs are when you have multiple ideas in a commit. We know what bad commit histories look like, and we're moving towards something where better commit histories make for easier code reviews. When you have to look at the end state, just to look at what changed, you haven't made a good story for someone else to review. If people start making histories that are more readable, I think code reviews will go a lot faster. That would be the benefit to writing good commit histories. The other benefit is git bisect when you're trying to learn how the code evolved to what it is today. If people write readable commits, they'll be able to understand why the code ended up the way that it is.

Refactoring Commits

Commits that don't alter execution flow
 * Moving code / Rearranging code commits
