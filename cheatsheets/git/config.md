# Enable signed commit with user key

Configure globally signing key identifier for user in Git:

```bash
git config --global user.signingkey <key ID>
```

Configure globally signed commits by default in Git (this setting makes use of `-s` flag unnecessary in theory):

```bash
git config --global commit.gpgsign true
```
