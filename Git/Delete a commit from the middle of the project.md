## Delete a commit from the middle of the project

Type in the terminal:

```
git rebase -i HEAD~5
```

This will get the last 5 commits, minus the current one, and will show them in a list.

Then you will navigate through the list using the up and down arrows, and type d and press enter on the ones you want to delete. You can't delete all of them from the list, you have to leave at least 1.

When you're done, type :wq and enter.

Then to force it to be sent to the repository (it will want to pull the old commits back, use:

```
git push —force origin mater
```