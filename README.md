# git-rebase
Git Rebase Training Repo

## Pair off and Branch

1. Pick a partner (or partners) & create a branch together.
1. Commit a few changes to your copy of that branch.
1. Pick someone to push their changes first.
1. Try to push the second person’s changes without merging/rebasing.

5. What does it tell you to do?
1. Can you remember the commandments?

7. Run the following to sync your branch with the origin & try to push again.
1. (Don't forget to replace `feature/my_branch` with your team's branch name)
```git pull --rebase origin feature/my_branch```

8. Run git log to look at your history
1. Repeat but swap the roles (you can reuse your branch).

## Rewrite history

1. On the same branch but on your own, commit a few changes to your copy of that branch.
Run:
```git rebase -i HEAD~N```
1. Where N is the number of commits back you’d like to edit the history from.

1. Read the prompt here, play with your history. Shuffle the order around, delete stuff, modify a commit, if you’re bored, try to add a new commit between two old commits.
1. Follow git’s instructions on how to apply your rebase
(Hint: if you get stuck, run git rebase --abort and go again).

1. Run git log & git show <commit_id> to see your new history!


## Break Things

1. In your groups again, pick one person to push their changes from the last step. (If this push doesn’t need a force push, you didn’t play with rebase enough :) use the other person’s changes or play with rebase some more)
1. Repeat the steps from the first exercise to try to push the next person’s changes.
1. What happens?

1. Force push the second person’s changes.
1. What happens to the history?
1. Try to use the following commands to push both of your changes (this may not be 100% possible, but get as close as you can).
```
git branch
git cherry-pick
```

## Don't be afraid to fail

1. Run git reflog
1. What do you see?
1. Recover (cherry pick) a change you deleted in the interactive rebase.


## Don't cross the streams (Don't mix rebase and merge)

1. Create a new branch
1. Commit a few times to the same file on both local master and the new branch.
1. Run git merge master from the new branch.
1. What happens when you now run git pull --rebase master from the new branch?


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
