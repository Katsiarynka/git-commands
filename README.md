# Git commands I use for productivity
Let's jump into a discussion how you can improve productivity if you're a developer.
In common, a usage of good tools and skill of using them can enhance productivity much faster. 
This tools are: Idle, and knowledge of how to work with it, make aliases in terminal, also terminal, 
knowledge of vim (Yeah, seriously), and the last one but not least - git commands.
So let's kick off this one and continue with another topics later. Follow me to see this topics.

Everyone knows how to watch git history:
```
git log
```
And, here another one that provides cool stat:
```
git log --stat 
```
Populars to check diff
```
# Check changes that was made locally, but not staged
git diff 
# with staged changes
git diff cached 
```
finally for getting diff of a commit in a terminal
```
git diff 48942..4af386f
```

To cache locale changes to get updates, f.e., from mainline:
```
git stash
# Store current work with untracked files
$ git stash -u
```
To upload changes in local branch:
```
git stash pop
```
I hope you make all your changes in mainline with one commit, 
and sometimes we share a branch with colleagues and to move all our code into a mainline, 
we need to pick some commits from this shared branch to mainline to make a final one pull request. You can use:
```
git log
git checkout mainline
git cherry-pick e12724…52a0
```
It's a little bit annoying if you have a lot of commits, so I prefer for this purposes:
```
git checkout mainline
git rebase shared
# change a cursor on HEAD of git commits, to get all changes unstaged and to make a beatifull commit
git reset HEAD~5 
# review all changes with git diff and make changes if necessary
git commit -a -m "All changes with a beatiful one commit"
```
And the final one, how to clean your local changes, rewrite working tree from specified commit
```
git reset --hard [commit]
```

Have a good git experience! 
Share you ideas what is you favorite git commands.