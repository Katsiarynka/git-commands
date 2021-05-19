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
git diff \\ Check changes that was made locally, but not staged
git diff cached \\  with staged changes
```
finally for getting diff of a commit in a terminal
```
git diff 48942192c9020ad407d354d1dd892db8d4af386f
```

To cache locale changes to get updates, f.e., from mainline:
```
git stash
```
To upload changes in local branch:
```
git stash pop
```

Sometimes we share a branch with colleagues and make a lot of commands into not a final branch, and we want to pick some commits from this branch to mainline to make a final one pull request. You can use:
```
git log
git checkout mainline
git cherry-pick e12724…52a0
```
It's a little bit a long way, so I'm 