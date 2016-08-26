Code Bombs
==========

We've often heard, "If you don't use it, you lose it." That's true of code. If you haven't used a piece of code in a while, then you'll need to refresh/relearn the code if you need it again.

How do you make it easier on yourself?

`git blame`

`gitk -- /path/to/file`

Your commit messages are like notes to yourself. Let them help you refresh your memory if you return to that area of the code base.


If you can't describe what you're doing, then how are you

When learning what to do, it's sometimes easier to learn from what not to do.

 * Code bombs are when you have multiple ideas in a commit. We know what bad commit histories look like, and we're moving towards something where better commit histories make for easier code reviews. When you have to look at the end state, just to look at what changed, you haven't made a good story for someone else to review. If people start making histories that are more readable, I think code reviews will go a lot faster. That would be the benefit to writing good commit histories. The other benefit is git bisect when you're trying to learn how the code evolved to what it is today. If people write readable commits, they'll be able to understand why the code ended up the way that it is.

Code bombs are an explosion of thoughts. Anyone looking at such disasters will have to piece together what happened. ... extend this metaphor?
