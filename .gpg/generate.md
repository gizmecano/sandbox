# Generate GPG key using terminal

```bash
$ gpg --armor --export <key ID>
$ git config --global user.signingkey <key ID>
$ git config --global commit.gpgsign true
```

# Edit existing key passphrase

Reference: [gpg remove passphrase](https://superuser.com/a/1488214/938540)

```bash
$ gpg --list-secret-keys
$ gpg --edit-key <key ID>
$ gpg> passwd
```
