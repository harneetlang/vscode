# Harneet Language Support for VS Code

Syntax highlighting and basic language configuration for the Harneet programming language (.ha).

## Features

- Syntax highlighting via TextMate grammar
- Language configuration for comments, brackets, and auto-closing pairs
- File association for `.ha`

## File structure

- `package.json` — VS Code extension manifest (contributes language + grammar)
- `syntaxes/harneet.tmLanguage.json` — TextMate grammar
- `language-configuration.json` — Comment styles, brackets, auto-close pairs
- `README.md` — This file

## Install (Development)

Option A: Launch an Extension Development Host
1. Open this folder in VS Code: `File → Open Folder…` and select `harneet_org/vscode/`.
2. Press `F5` (Run → Start Debugging) to launch a new VS Code window with the extension loaded.
3. Open a `.ha` file — it should be highlighted as Harneet.

Option B: Package and install as VSIX
1. Install VSCE if you don't have it:
   ```bash
   npm install -g @vscode/vsce
   ```
2. From this folder, run:
   ```bash
   vsce package
   ```
   This creates a `.vsix` file (e.g., `harneet-language-support-0.0.1.vsix`).
3. In VS Code, run `Extensions: Install from VSIX...` and select the generated `.vsix`.

## Known grammar highlights

- Line comments: `// ...`
- Block comments: `/* ... */`
- Strings: double-quoted with escapes
- Numbers: integers and floats
- Keywords: `var`, `function`, `type`, `struct`, `import`, control-flow keywords
- Builtins (basic): `range`, `enumerate`, `len`
- Module functions: `module.member(...)` (e.g., `fmt.Printf(...)`)

## License

MIT
