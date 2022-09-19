# Handle git tags

## Create a signed tag

```bash
# Create a signed tag:
$ git tag -s <tag_name> -m 'Message about the tag'
# Push a signed tag to remote:
$ git push origin <tag_name>
```

## Remove a tag

```bash
# Delete a local tag:
$ git tag -d <tag_name>
# Delete a remote tag:
$ git push --delete origin <tag_name>
# Delete a remote tag (alternative method):
$ git push origin :refs/tags/<tag_name>
```

## Create a branch for a specific tag

A helpful command for properly tracking specific releases of a project using git tags.

```bash
# List all the tags:
$ git tag -l
# Create a new branch directly for a specific tag:
$ git checkout tags/<tag_name> -b <branch_name>
```

Alternatively, it's possible to only checkout the tag, but the pointer will be on a branch named after the revision number of tag.

```bash
# Checkout a specific tag:
$ git checkout tags/<tag_name>
```

For reference, _cf._ [_Download a specific tag with Git_](https://stackoverflow.com/a/792027) by [Renato Besen](https://github.com/besen/) [CC BY-SA 2.5](https://creativecommons.org/licenses/by-sa/2.5/)

## Change the date of a tag

The procedure below aims to change the date of a specific tag (_e.g._ when sorting of these tags is not properly preserved after pushing to a remote repository such as GitHub). It partially repeats commands which were mentionned about [removing a tag](##remove-a-tag).

```bash
# Checkout the commit associated with the tag:
$ git checkout <tag_name>
# Delete the local tag:
$ git tag -d <tag_name>
# Delete the remote tag:
$ git push --delete origin <tag_name>
# Create the revised tag with a date based from the head of the current checkout:
$ GIT_COMMITTER_DATE="$(git show --format=%aD  | head -1)" git tag -a <tag_name> -m "Add retroactively a tag for version <tag_name>"
# Push revised tags
$ git push -taggs
```

For reference, _cf._ [_Change date of git tag (or GitHub Release based on it)_](https://stackoverflow.com/a/21741848) by [Gavin Kistner](https://github.com/Phrogz) [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)
