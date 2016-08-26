Commit Types
============


Oftentimes when you need to update code, the surrounding code will need some massaging (a.k.a. minor refactoring).


If you live by the boy scout rule, whenever you visit an area of the codebase, you leave it better than you found it. If you're fixing a bug or implementing a new feature, don't combine refactoring with your actual bug fix or new-feature code. Keep them separate!

Fixing warnings
===============

If you're fixing warnings or FindBugs, make that a separate commit.

You might tackle more than one type of warning, such broad sweeping commits will have commit messages like


If the fixes are in separate parts of a file or in different files altogether and there is no broad, thematic FindBug your fixing. You might tackle more than one type of warning in a commit. Be careful here though. You might want to separate each type of warning in a separate commit for clarity. Now you don't have to go as far as 

It depends on how clear you want your commit to be




Fix multiple warnings of various types in one or many files.

```
Fixed FindBugs

 * instanceof will always return false (BC_IMPOSSIBLE_INSTANCEOF)
 * Impossible cast (BC_IMPOSSIBLE_CAST)
```
```
Fixed Eclipse warnings

 * Resource not managed via try-with-resource
 * Usage of a raw type
```
```
Fix multiple warnings of the same type in one or many files.
```
Fixed FindBug "instanceof will always return false (BC_IMPOSSIBLE_INSTANCEOF)"```
```
```
Fix multiple warnings of the same type in one file.
```
Fixed FindBug "instanceof will always return false (BC_IMPOSSIBLE_INSTANCEOF)" in ClassWithFindBug
```
```
Fixed FindBug "instanceof will always return false (BC_IMPOSSIBLE_INSTANCEOF)" in AnotherClassWithFindBug
```

To make it easier on someone reviewing the a fix-warnings commit, you may want to separate warnings fixes that change code execution vs. warnings fixes that are more cosmetic.

Example of code execution change
```
Writer writer = null;
try {
	writer = new BufferedWriter(file);
	writer.write("Example writing is so...");
} finally {
	writer.close();
}
```
to
```
try (Writer writer = new BufferedWriter(file)) {
	writer.write("Example writing is so...");
}
```

Example of cosmetic change
`List<String> str = new ArrayList<String>()` to `List<String> str = new ArrayList<>()`

When code reviewing this type of commit, look for patterns. For certain types of warnings fixes, you can quickly.

Adding code
===========

When adding new code, ideally gitk will be all green signaling the addition of code.

There are times when gitk won't be all green though. This includes:

 * adding arguments to methods (Inject Dependency Commit)



Deleting code
=============

When deleting code, ideally gitk will be all red signaling the deletion of code.

Nothing makes me happier than deleting code. Dead code is clutter.

Sometimes your IDE will warn you about dead code. If it does, then your deleting-code commit is also a fixings-warnings commit.

After replacing/moving code, you 

https://en.wikipedia.org/wiki/Dead_code

Thou shalt delete all dead, uselsee code! Please, just trust me. It will save you a lot of maintenance nightmares in the future if you do.

In this type of commit, all you should be doing is deleting lines of code.

Ideally, gitk should be all red.





Java-specific: Organizing imports
=================================

In Eclipse, you can organize your imports of your Java class


Formatting
==========


 * Organizing imports
 * Formatting
 * Moving/Rearranging code
 * Replace code


 * Inject Dependency Commit

With this commit type, you'll be getting a dependency from point A to point B.
Your commit messages will be like

This commit can often be

Example commit messages:


Injected height into Tuple





Code Reviewer: You'll


 * New Code Commit (all green in gitk)
 * Dead Code Commit
 * Hookup Commit

 * Commits to highlight the discussion
 * Break formatting for clarity

Commits that don't alter execution flow
 * Moving code / Rearranging code commits

 * Action commit
 
  * Fixed bug
 