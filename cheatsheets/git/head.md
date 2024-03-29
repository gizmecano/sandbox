# Set properly `origin/HEAD`

By default, `origin/HEAD` will be the branch which is checked out when cloning. In order to properly set this branch (_e.g._ if it has been amended in the admin settings of a repository for a fork), the command below can be used:

```bash
git remote set-head origin <branch_name>
```

The `origin/HEAD` branch can be remove using:

```bash
git remote set-head origin -d
```

For reference, _cf._ [_Why is "origin/HEAD" shown when running "git branch -r"?_](https://stackoverflow.com/a/6838756) by [Christopher Dunn](https://github.com/cdunn2001) [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)
