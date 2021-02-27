# language-mplus README

A syntax highlither for Mplus input and output files.

## Features

It highlights Mplus code.

## Task

I haven't figured out how to set up a custom builded for VS code. This task
works for me:

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
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
```

Just make sure to point to the actual mplsu executable path in this line:
`"command": "mplus",`.

## License - MIT

This software is released under MIT license.

Copyright 2021

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
