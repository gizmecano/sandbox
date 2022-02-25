# Manage signed tag

## Create signed tag

```bash
# Create a signed tag:
$ git tag -s tagname -m 'Message about the tag'
# Push the signed tag to remote:
$ git push origin tagname
```

## Remove tag (locally and remotely)

```bash
# Delete local tag:
$ git tag -d tagname
# Delete remote tag:
$ git push --delete origin tagname
# Delete remote tag (alternative method):
$ git push origin :refs/tags/tagname
```

## Create a branch for a specific tag

A helpful command for properly tracking specific releases of a project using git tags. [Reference](https://stackoverflow.com/a/792027/4094098)

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
