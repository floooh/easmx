# easmx
A fork of the asmx assembler, slightly extended for the [VSCode KC IDE extension](https://github.com/floooh/vscode-kcide).

## What's new:

- use cmake as build system with a WASI build preset
- split build into a library and executable
- `incbin` opens files in binary mode (`rb`)
- add a `-i [dir]` cmdline option to provide a root directory for includes (important
  for platforms without the concept of a current working directory, like WASI)
- add a `-m [filename]` cmdline option to generate a .map file (maps machine code addresses back to source files and line numbers)
