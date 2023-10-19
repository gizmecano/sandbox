# GNU Privacy Guard

## Generate key

Export a key in a binary format:

```bash
gpg --armor --export <key ID>
```

## Edit existing key passphrase

List existing stored keys:

```bash
gpg --list-secret-keys
```

Open edition menu for modify specified key:

```bash
gpg --edit-key <key ID>
```

Change key password at the prompt:

```bash
gpg> passwd
```

For reference, _cf._ [_gpg remove passphrase_](https://superuser.com/a/1488214) by [Frak](https://github.com/frakman1) [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
