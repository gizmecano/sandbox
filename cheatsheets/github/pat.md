# Personal access token

At this time, a GitHub _personal access token_ (PAT) is a 40 characters string (the first 4 ones seem to always appear to be `ghp_` at this time), such as `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`.

## Configure a PAT in SourceTree

In the project settings, change the `origin` path value by adding the personal access token string followed by the `@` sign before the web URL of the repository, such as:

[https://github.com/username/repository.git](https://ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx@github.com/username/repository.git)

## Configure a PAT in Visual Studio Code

Set a GitHub a remote personal access token to Visual Studio Code (prompt this command in the terminal panel of the project directory):

```bash
git remote set-url origin https://<username>:ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx@github.com/<username>/<repository>.git
```

For reference, _cf._ [_How to add a GitHub personal access token to Visual Studio Code_](https://stackoverflow.com/a/66830126) by [Giddy Naya](https://github.com/GiddyNaya) [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
