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
