title: How Do You Rewrite a Project From Scratch Once It's On GitHub?
date: 2014-08-14 10:04
categories: python sandman git

Rather than an information-laden article, this post is a real question about a
situation I'm currently in and need help with. The setup is simple: I have a
project ([sandman](http://www.github.com/jeffknupp/sandman)) on GitHub with a
reasonably long commit history and list of contributors. I've re-written the
project from scratch. It shares no git history with the original project. How do
I make the new project the official version (without offending those who
contributed to the original one)?

<!--more-->
## My Choices

As I see it, I have three choices. The first is just to delete the old repo,
rename the new repo, and call it a day. None of the old project will be
preserved. On a positive note, however, the commit history will be clean and
accurate, and reflect exactly what work was done on the project.

Or I could "migrate" the old project to the new one, by simply adding the new
files in the old repo and deleting any others that are no longer used (almost
all of the old files). In this way, I keep the commit history and contributors
of the original project, but at the cost of a weird history that doesn't make
much sense. It would really be the history of two separate projects spliced
together at a specific point.

The third choice, of course, is to just keep the old project the way it is and
not use the rewrite. Each day that goes by, though, this seems less and less
viable a solution, as the new project is almost at feature parity with the old.
That brings me to another question:

## Versioning and Backwards Incompatibility

How do I version the new project? The old project never hit 1.0 and thus it
could be argued the API was always open to breaking changes, but this isn't a
change to the API, it's an entirely new and different API. The current version
of `sandman` is something like `0.9.8`. If I replaced the old project with the
new one, what would the version be? Keep in mind that for PyPI, the version
would need to be *higher* than the version of the old project for PyPI to
consider the new package the latest version.

## HELP!

I'm really kind of stuck here, which is why I'm asking for help. My hope is
someone much smarter than me sees another solution, or a better way to implement
one of the ones I mentioned. So please, if you have any ideas, let me know! Feel
free to either leave a comment here or in the thread on [Chat For Smart People](http://discourse.jeffknupp.com).
