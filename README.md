# language-mplus README

A syntax highlither for Mplus input and output files.

## Features

It highlights Mplus code.

## Task

Add a build task to be able to automatically run mplus in the built-in VS Code terminal.

Click on Terminal -> Configure Tasks and copy and paste the build task below:

```
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    // See https://code.visualstudio.com/docs/editor/variables-reference
    // for variable reference
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Run Mplus",
            "type": "process",
            "command": "mplus",
            "args": ["${fileBasename}"],
            "options": {
                "cwd": "${fileDirname}"
            },
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
```

Just make sure to point to the actual mplus executable path in this line:
`"command": "mplus",`.

Keep in mind that mplus should add itself to the path when installing it. If you run into
problems with it, make sure to replace `mplus` with the actual path to the binary file.

## Attribution

The code for this syntax highlighter was inspired and based upon [this plugin for Sublime Text 2
by bkeller2](https://github.com/bkeller2/Mplus).

## License - Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)

This is a human-readable summary of (and not a substitute for) the license. Disclaimer.

You are free to:

- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

- Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- NonCommercial — You may not use the material for commercial purposes.
- ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
- No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

[See this page](https://creativecommons.org/licenses/by-nc-sa/4.0/) for the full license.
