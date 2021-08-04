# Generate GPG key using terminal

```bash
$ gpg --armor --export <key ID>
$ git config --global user.signingkey <key ID>
$ git config --global commit.gpgsign true
```
