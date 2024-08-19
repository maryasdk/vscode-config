# Vscode Configuration

Personal Preferences for my Vscode Configuration, mainly focused on React development.

## Directory layout

    .
    ├── user-settings.jsonc
    ├── list-extensions.txt
    ├── LICENSE
    └── README.md

## Useful Commands

```bash
code --list-extensions
```

Lists extensions currently installed in VSCode

---

```bash
code --list-extensions --show-versions
```

Lists extensions currently installed in VSCode with their versions

---

```bash
code --install-extension (<extension-id> | <extension-vsix-path>)
```

Installs a specific extension

---

`Ctrl+Shift+P` -> `Preferences: Open User Settings (JSON)`

Opens the VSCode command palette and then the user settings in json format

## Using the Configuration

### Importing the Extensions

First, either export the latest extensions list from the previous machine with the "install-extension" prefix using the below command:

Unix:

```bash
code --list-extensions | xargs -L 1 echo code --install-extension
```

Windows PowerShell:

```
code --list-extensions | % { "code --install-extension $_" }
```

Or just use the list-extensions.txt file, prefix "code --install-extension" to each line, and then run the instal commands on your new machine.

Sample output:

```bash
code --install-extension dbaeumer.vscode-eslint
code --install-extension wallabyjs.quokka-vscode
```

### Importing the Settings

1. Copy the content of `user-settings.jsonc`
2. Open the VSCode user settings file on your machine
3. Paste the content to compeletely override the settings
