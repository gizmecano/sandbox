# Personal access token

At this time, a GitHub _personal access token_ (PAT) is a 40 characters string (the first 4 ones seem to always appear to be `ghp_` at this time), such as `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`.

## Configure a PAT in SourceTree

In the project settings, change the `origin` path value by adding the personal access token string followed by the `@` sign before the web URL of the repository, such as:

[https://github.com/username/repository.git](https://ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx@github.com/username/repository.git)
