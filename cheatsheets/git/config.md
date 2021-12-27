# Enable signed commit with user key

```bash
# Configure globally signing key identifier for user in Git:
$ git config --global user.signingkey <key ID>

# Configure globally signed commits by default in Git:
$ git config --global commit.gpgsign true
# (this setting makes use of `-s` flag unnecessary in theory)
```
