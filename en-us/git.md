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


###### Linking to files on github

Simple use case: you want to refer to somethign in a repository, by simply dropping a link to github.

By default, when browsing the master branch, your URL will contain something like
blob / master etc. Obviously, in the future, e.g. two years from now, the contents of the master branch could easily change. 

To make your link more permanant, such that someone finding your link years later (like in the case of a historical Jira comment, or notes, etc.)
you can change the default link to explicitly represent the current commit.

This is a good practice, as you'll never know when you'll be referring to past
details in the future.

Look for the commit abbreviation in the header section above the file listing,
e.g. a536100 on Jun 28. Click that and you'll load that commit, where you can
copy and paste the whole commit it.

    Change this format:
    https://github.com/{user}/{repository}/blob/master/{file path}
    to this:
    https://github.com/{user}/{repository}/blob/{commit id}/{file path}
