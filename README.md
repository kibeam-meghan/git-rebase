# git-rebase
Git Rebase Training Repo

## Pair off and Branch

Pick a partner (or partners) & create a branch together.
Commit a few changes to your copy of that branch.
Pick someone to push their changes first.
Try to push the second person’s changes without merging/rebasing.

What does it tell you to do?
Can you remember the commandments?

Run the following to sync your branch with the origin & try to push again.
(Don't forget to replace `feature/my_branch` with your team's branch name)
```git pull --rebase origin feature/my_branch```

Run git log to look at your history
Repeat but swap the roles (you can reuse your branch).

## Rewrite history

On the same branch but on your own, commit a few changes to your copy of that branch.
Run:
```git rebase -i HEAD~N```
Where N is the number of commits back you’d like to edit the history from.

Read the prompt here, play with your history. Shuffle the order around, delete stuff, modify a commit, if you’re bored, try to add a new commit between two old commits.
Follow git’s instructions on how to apply your rebase
(Hint: if you get stuck, run git rebase --abort and go again).

Run git log & git show <commit_id> to see your new history!


## Break Things

In your groups again, pick one person to push their changes from the last step. (If this push doesn’t need a force push, you didn’t play with rebase enough :) use the other person’s changes or play with rebase some more)
Repeat the steps from the first exercise to try to push the next person’s changes.
What happens?

Force push the second person’s changes.
What happens to the history?
Try to use the following commands to push both of your changes (this may not be 100% possible, but get as close as you can).
```
git branch
git cherry-pick
```

## Don't be afraid to fail

Run git reflog
What do you see?
Recover (cherry pick) a change you deleted in the interactive rebase.


## Don't cross the streams (Don't mix rebase and merge)

Create a new branch
Commit a few times to the same file on both local master and the new branch.
Run git merge master from the new branch.
What happens when you now run git pull --rebase master from the new branch?


## Other nice git cammands that can improve legibility
```
git commit -p
git add -p
git diff --cached
git show
```

## Further Reading

Official git docs:

https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

https://git-scm.com/docs/git-merge

https://git-scm.com/docs/git-rebase

Good Atlassian tutorial with great images:

https://www.atlassian.com/git/tutorials/using-branches/git-merge
