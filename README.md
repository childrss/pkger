# pkger

pkger creates a macOS installer file that executes a given script, and creates an install receipt.

## Example usage

Create a script called `demo.sh`:

```
#!/bin/bash

say "ATLAS rocks!"
```

Execute

```
docker run --rm -it -v `pwd`:/data pkger demo.sh uiucatlas/pkger demo.sh com.illinois.atlas.demo 1.0
```

This will create the installer package `demo.sh.pkg` in your current directory. That's it!
