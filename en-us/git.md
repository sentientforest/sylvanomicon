### Git

Some advice: use git a lot.

From The Pragmatic Progammer:

> Tip 23: Always Use Source Control
> ...
> Even if the stuff you're working on isn't source code.

Andrew Hunt & David Thomas, (2000) _The Pragmatic Programmer_, page 88
or
David Thomas & Andrew Hunt, (2020) _The Pragmatic Programmer 20th Anniversary Edition_, page 85

Case in point, this notes repository...

#### notes on usage

###### Check first ever commit in a repository

    git log --reverse

###### Undoing a repository

I recently started a "tutorials" repository to collect various tutorials I do
in one place. I wanted to keep them all under version control in one reposiotry.
Certain tutorials or commands that initialize a project will automatically make
the project directory a git repository. Since my parent directory is already a
single git repository, this is unnecessary and can lead to confusion as to
where to commit.

I was pretty sure this would be how to accomplish the goal of "undoing git init",
but wanted to double check.

https://stackoverflow.com/questions/4754152/how-do-i-remove-version-tracking-from-a-project-cloned-from-git

    rm -rf .git

This will essentially remove all the git history in the auto-generated
tutorial project. Then in the parent directory, we can add the files as normal.
This gives me a single git repository with all the tutuorials I have walked
through in one place, and makes it more easier to see what was done when.
