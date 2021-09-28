# Folder settings

This file deals with applied [settings to a specific folder](https://code.visualstudio.com/docs/getstarted/settings#_settings-precedence) (in a multi-root workspace) which override generic user and workspace ones.

## Editor

```json
"editor.bracketPairColorization.enabled": true,
"editor.renderWhitespace": "all",
"editor.rulers": [
  80
],
"editor.wordWrap": "wordWrapColumn",
"editor.wordWrapColumn": 80,
```

## Files

```json
"files.exclude": {
  "**/desktop.ini": true
},
```

```json
"files.trimTrailingWhitespace": true,
```

## Git

```json
"git.enableCommitSigning": true,
```

## Search

```json
"search.useIgnoreFiles": false,
```

## Overridden settings

### Markdown

```json
"[markdown]": {
  "editor.wordWrap": "wordWrapColumn",
  "editor.wordWrapColumn": 80,
  "files.trimTrailingWhitespace": false
},
```
