Code Bombs

Clean Commits


Clean Commit Histories Speed Up Code Review

Communication - Help Communicate Why You're Doing Something



Merge small things faster



Every commit should be compilable and unit testable. This might not apply to interpreted languages.
====================================================

Although this might not be possible in every case, it's an ideal to strive for.


 * Should I apply these principles when starting a new project?




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
