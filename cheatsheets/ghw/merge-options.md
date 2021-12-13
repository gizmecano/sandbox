# Merge button options

According to _Merge button_ section in _Settings_ panel:

> When merging pull requests, you can allow any combination of merge commits, squashing, or rebasing. At least one option must be enabled. If you have linear history requirement enabled on any protected branch, you must enable squashing or rebasing.

## Allow merge commits

> Add all commits from the head branch to the base branch with a merge commit.

**Create a merge commit**: all commits from the branch `issue/${issueNumber}` will be added to the base branch `draft` via a merge commit.

## Allow squash merging

> Combine all commits from the head branch into a single commit in the base branch.

**Squash and merge**: the commits from the branch `issue/${issueNumber}` will be combined into one commit on the base branch `draft`.
