# GNU Privacy Guard

## Generate key

```bash
#
$ gpg --armor --export <key ID>
```

## Edit existing key passphrase

Reference: [gpg remove passphrase](https://superuser.com/a/1488214/938540)

```bash
#
$ gpg --list-secret-keys
#
$ gpg --edit-key <key ID>
#
$ gpg> passwd
```
