# GNU Privacy Guard

## Generate key

```bash
# Export a key in a binary format:
$ gpg --armor --export <key ID>
```

## Edit existing key passphrase

```bash
# List existing stored keys:
$ gpg --list-secret-keys
# Open edition menu for modify specified key:
$ gpg --edit-key <key ID>
# Change key password at the prompt:
$ gpg> passwd
```

For reference, _cf._ [_gpg remove passphrase_](https://superuser.com/a/1488214) by @frakman1 [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
