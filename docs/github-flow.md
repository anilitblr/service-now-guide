# GitHub Flow

The following is the ServiceNow specific version of GitHub flow.

# Create a new branch

Start by pulling any updates to the `main` branch

```
git checkout main

git pull

git checkout -b <new branch name>
```

# Make your edits

Write your new code in the branch that you created above. Commit your changes, but don't push yet.

```
git add <list your files here>

git commit
```

Then write a descriptive messages describing what updates you have made.

Use `closes #1` to close an issue with id = 1. Or write `fixes #2` when you are fixing a bug with issue id = 2.

Obviously, change the IDs above to be the issue(s) that you are working on in this branch.

# Rebase your branch with any updates to main

It is important that you test your changes against the current version of `main`. As you've been working it's likely
that the `main` branch was being updated. So, you must get all updates to `main` and test your branch against the newest
updates to `main`.

```
git checkout main

git pull

git checkout <new branch name>

git rebase main
```

# Test your updates again

Now, test your edits against the latest version of `main`. When you have verified that everything works, the next step
is to push your updates.

```
git push --set-upstream origin <new branch name>
```

# Now open a pull request (PR)
