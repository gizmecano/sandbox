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
