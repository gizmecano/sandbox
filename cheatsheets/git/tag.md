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

For reference, _cf._ [_Download a specific tag with Git_](https://stackoverflow.com/a/792027)
