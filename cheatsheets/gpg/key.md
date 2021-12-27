# GNU Privacy Guard

## Generate key

```bash
# Export a key in a binary format:
$ gpg --armor --export <key ID>
```

## Edit existing key passphrase

Reference: [gpg remove passphrase](https://superuser.com/a/1488214/938540)

```bash
# List existing stored keys:
$ gpg --list-secret-keys
# Open edition menu for modify specified key:
$ gpg --edit-key <key ID>
# Change key password at the prompt:
$ gpg> passwd
```
