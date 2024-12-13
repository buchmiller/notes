# Git

## Update commit dates

See <https://graphite.dev/guides/git-commit-date#changing-commit-dates>

On your feature branch, commit whenever you want. Right before doing a pull request/merge, run this command to set all the commit dates to now:

`git rebase origin/master --exec "git commit --amend --no-edit --date=now"`

(requires at least Git v2.1.4)

and then this to override the remote commits for your branch:

`git push --force`

To change to a specific date:

`git rebase origin/master --exec "git commit --amend --no-edit --date="Fri Oct 31 14:00 1975 +0100""`

## Create hotfix

Create a new branch based on the released tag that needs the fix.

```bash
git fetch --tags
git checkout -b hotfix/1-21-fix tags/1.21.0
```

After adding the fix, merge the branch to main branch, but do not delete the branch yet.

Create a new tag directly from the hotfix branch.

```bash
git tag 1.21.1
git push origin 1.21.1
```
