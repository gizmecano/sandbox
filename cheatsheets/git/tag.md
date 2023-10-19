# Handle Git tags

## Sign a tag

Create a signed tag (the `-m` option may be used to supplement the log message of the created commit):

```bash
git tag -s <tag_name> -m 'Message about the tag'
```

Push a signed tag to remote repository:

```bash
git push origin <tag_name>
```

## Delete a tag

Delete a local tag:

```bash
git tag -d <tag_name>
```

Push a deleted tag to remote repository in order to remove it:

```bash
git push --delete origin <tag_name>
```

## Checkout a tag

Create a new branch directly for a specific tag (helpful for properly tracking specific releases of a project using git tags):

```bash
git checkout tags/<tag_name> -b <branch_name>
```

Alternatively, it's possible to only checkout a tag (but the pointer will be on a branch named after the revision number of tag):

```bash
git checkout tags/<tag_name>
```

For reference, _cf._ [_Download a specific tag with Git_](https://stackoverflow.com/a/792027) by [Renato Besen](https://github.com/besen/) [CC BY-SA 2.5](https://creativecommons.org/licenses/by-sa/2.5/)

## Change a tag date

Change the date of a specific tag (_e.g._ when sorting of tags is not properly preserved after pushing to remote repository).

Checkout the commit associated with the tag:

```bash
git checkout <tag_name>
```

Delete the local tag:

```bash
git tag -d <tag_name>
```

Delete the remote tag:

```bash
git push --delete origin <tag_name>
```

Create the revised tag with a date based from the head of the current checkout:

```bash
GIT_COMMITTER_DATE="$(git show --format=%aD  | head -1)" git tag -a <tag_name> -m "Add retroactively a tag for version <tag_name>"
```

Push the revised tags:

```bash
git push -tags
```

For reference, _cf._ [_Change date of git tag (or GitHub Release based on it)_](https://stackoverflow.com/a/21741848) by [Gavin Kistner](https://github.com/Phrogz) [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)
