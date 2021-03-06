# Merge button options

According to _Merge button_ section in _Settings_ panel:

> When merging pull requests, you can allow any combination of merge commits, squashing, or rebasing. At least one option must be enabled. If you have linear history requirement enabled on any protected branch, you must enable squashing or rebasing.

The three available options listed below have been tested during the [second phase](https://github.com/gizmecano/sandbox/issues/7):

- [_Merge commit_](https://github.com/gizmecano/sandbox/pull/8)
- [_Squash and merge_](https://github.com/gizmecano/sandbox/pull/9)
- [_Rebase and merge_](https://github.com/gizmecano/sandbox/pull/10))

## Allow merge commits

> Add all commits from the head branch to the base branch with a merge commit.

**Create a merge commit**: all commits from the branch `issue/${issueNumber}` will be added to the base branch `draft` via a merge commit.

## Allow squash merging

> Combine all commits from the head branch into a single commit in the base branch.

**Squash and merge**: the commits from the branch `issue/${issueNumber}` will be combined into one commit on the base branch `draft`.

## Allow rebase merging

> Add all commits from the head branch onto the base branch individually.

**Rebase and merge**: the commits from the branch `issue/${issueNumber}` will be rebased and added to the base branch `draft`.
