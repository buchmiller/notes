# Git

## Show commit details

Show name and date for both author and commit on all commits:

`git log --format=fuller`

Show only for most recent commit (multiple options):

```shell
git log --format=fuller -n 1 # limit to 1
git show -s --format=fuller # -s suppresses diff output
```

Can also use any of those for specific commit hash by including it at the end of the command.

## Update previous commits

See <https://graphite.dev/guides/git-commit-date#changing-commit-dates>

### Author vs Commit

The commands from [above](#show-commit-details) will display two types of name and date.

- Author name/date: Who originally made the changes and when.
- Commit name/date: Who last applied changes and when, such as with a rebase or amend.

For example running `git show -s --format=fuller` might show something like this:

```console
commit 3e9584744656eb008d69f3247037a08ea9a854ea
Author:     Bob Butler <bob@example.com>
AuthorDate: Fri Feb 21 11:24:39 2025 -0700
Commit:     John Smith <john@example.com>
CommitDate: Mon Feb 24 07:41:51 2025 -0700

    Fixed the test output.
```

We can see that Bob originally made the change on Feb 21, but John actually committed the changes to the repository on Feb 24.

The committer may be different from the author if the changes were pulled from a patch or another branch. It may also indicate an amended commit, perhaps from a rebase.

### Change commit info

To change the committer name and date (and keep original author info):

`GIT_COMMITTER_NAME="Bob Butler <bob@example.com>" GIT_COMMITTER_DATE="2025-02-12 10:30" git commit --amend --no-edit`

To change author name and date:

`git commit --amend --no-edit --author="Bob Butler <bob@example.com>" --date="2025-02-12 10:30"`

To change an older commit, you'll need to use an interactive rebase:

```console
// use the hash of the commit before the one you want to update
> git rebase -i hash

// change the option from pick to edit on the commits to change

// while paused on a commit to edit, amend the desired info
> git commit --amend --date=now

// continue with the rebase
> git rebase --continue

// force update origin with the modified commit history
> git push --force
```

### Update multiple commit dates with rebase

On your feature branch, commit whenever you want. Right before doing a pull request/merge, run this command to set all the commit dates to now:

`git rebase origin/master --exec "git commit --amend --no-edit --date=now"`

(requires at least Git v2.1.4)

and then this to override the remote commits for your branch:

`git push --force`

To change to a specific date:

`git rebase origin/master --exec "git commit --amend --no-edit --date="2025-01-01 14:00""`

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
