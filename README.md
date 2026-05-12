[Japanese README](README.ja.md)

[![Version](https://img.shields.io/badge/version-v0.3.10-4094ff.svg)](https://marketplace.visualstudio.com/items?itemName=komiyamma.commit-message-gene-by-gemini-cli)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
![Windows 10|11](https://img.shields.io/badge/Windows-_10_|_11-6479ff.svg?logo=windows&logoColor=white)

Primary target: VS Code-compatible editors such as VS Code, VSCodium, Kiro, and Antigravity.

# Commit Message Generator (by Gemini)

This extension automatically generates a Conventional Commits-style commit message from your repository changes and inserts it into the Source Control input box.  
It uses the Gemini API through `@google/genai`. Set `GEMINI_API_KEY` or `GOOGLE_API_KEY` before starting your editor.

## Usage

- From the UI (recommended)
  - A button is added to the Source Control view title bar and near the commit input box. Click it to run "Commit message generation by Gemini."
  - It appears when the Git provider is active.  
  [![Commit Input Box Button](images/button.png)](images/button.png)
  - While generating, the status bar shows "$(sync~spin) Generating commit message..." and it disappears automatically when finished.  
  [![Commit StatusBar](images/statusbar.png)](images/statusbar.png)
- From the Command Palette
  - Press `Ctrl+Shift+P` and type "Commit message generation by Gemini".
  - Or run "Commit message generation by Gemini" (`commit-message-gene-by-gemini-cli.runGeminiCLICmd`) directly.
  - When finished, the generated message is inserted into the commit input box. If an error occurs, check the Output panel "commit message gene".

## Settings

- `commitMessageGeneGemini.prompt.intro.en`
- `commitMessageGeneGemini.prompt.intro.ja`

## Requirements

- VSCode with Git available in the workspace
- `GEMINI_API_KEY` or `GOOGLE_API_KEY` is set in the environment before the editor starts
- Built-in VSCode Git extension is enabled

## License

MIT License © 2025-2026 komiyamma
