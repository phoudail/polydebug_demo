# PolyDebug demo

This repository is a demo for the PolyDebug research tool, in the form of a VSCode extension.

# Build and run

You will need a working installation of docker, vscode, npm and yarn.

If you haven't already, update the submodules:

```bash
git submodule update --init --recursive
```

Build the actual PolyDebug tool:

```bash
docker build -t demo ./LiveProbes
```

Then build the extension:

```bash
cd vscode-polydebug/
yarn
```

Then open the `vscode-polydebug` folder with Visual Studio Code. In `src/mockDebug.ts`, replace the `workspacePath` variable (line 93) with your own location.
Go in the 'Run and Debug' side menu, select the 'Extension + Server' debug configuration and launch it. 
A new VSCode instance should open, in which you can set breakpoints and debug polyglot programs.