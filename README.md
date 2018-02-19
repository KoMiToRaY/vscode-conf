## General settings
```
{
  "atomKeymap.promptV3Features": true,
  "editor.multiCursorModifier": "ctrlCmd",
  "editor.formatOnPaste": false,
  "workbench.colorTheme": "Abyss",
  "workbench.iconTheme": "vscode-icons",
  "editor.renderWhitespace": "all",
  "editor.tabSize": 2,
  "editor.fontSize": 16,
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "terminal.integrated.shell.linux": "/usr/local/bin/bash-login",
  "[scss]": {

  }
}
```

## Keybindings.json
```
[
    {
        "key": "f5",
        "command": "editor.action.sortLinesAscending"
    }
]
```

## Install plugin

```.bash
code --install-extension extension_name

CraigMaslowski.erb
Tyriar.sort-lines
abusaidm.html-snippets
color-variable-replace.color-variable-replace
dbaeumer.vscode-eslint
formulahendry.auto-close-tag
glen-84.sass-lint
michelemelluso.code-beautifier
mrmlnc.vscode-scss
ms-vscode.atom-keybindings
octref.vetur
robertohuertasm.vscode-icons
samverschueren.final-newline
sianglim.slim
```

## Allow integrated terminal to run as login shell

https://github.com/Microsoft/vscode/issues/7263

Create a file named **/usr/local/bin/bash-login** and add the following lines to it (You might need **root** to create that file depending on your setup):

```.bash
#!/bin/bash
bash -l
```

Make it executable with 
> chmod +x /usr/local/bin/bash-login.

On your VSCode user settings, set:
```vscode
{
  "terminal.integrated.shell.linux": "/usr/local/bin/bash-login"
}
```
