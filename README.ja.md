[English README](README.md)

[![Version](https://img.shields.io/badge/version-v0.3.10-4094ff.svg)](https://marketplace.visualstudio.com/items?itemName=komiyamma.commit-message-gene-by-gemini-cli)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
![Windows 10|11](https://img.shields.io/badge/Windows-_10_|_11-6479ff.svg?logo=windows&logoColor=white)

主な対象は VS Code 互換エディタです。特に VS Code、VSCodium、Kiro、Antigravity を想定しています。

# コミットメッセージジェネレーター (by Gemini)

この拡張は、リポジトリの変更から Conventional Commits 形式のコミットメッセージを自動生成して、ソース管理の入力欄へ挿入します。  
`@google/genai` 経由で Gemini API を使います。エディタを起動する前に `GEMINI_API_KEY` または `GOOGLE_API_KEY` を設定してください。

## 使い方

- UI から（推奨）
  - ソース管理ビューのタイトルバーとコミット入力欄の近くにボタンが追加されます。クリックで「Commit message generation by Gemini」を実行します。
  - Git プロバイダーが有効な場合に表示されます。  
  [![Commit Input Box Button](images/button.png)](images/button.png)
  - 生成中はステータスバーに「$(sync~spin) Generating commit message...」が表示され、完了時に自動で消えます。  
  [![Commit StatusBar](images/statusbar.png)](images/statusbar.png)
- コマンドパレットから
  - `Ctrl+Shift+P` → 「Commit message generation by Gemini」と入力
  - あるいは「Commit message generation by Gemini」(`commit-message-gene-by-gemini-cli.runGeminiCLICmd`) を直接実行
  - 完了すると、生成メッセージはコミット入力欄に挿入されます。エラーが起きた場合は Output パネル「commit message gene」を確認してください。

## 設定

- `commitMessageGeneGemini.prompt.intro.en`
- `commitMessageGeneGemini.prompt.intro.ja`

## 要件

- VSCode と Git が利用できること
- エディタを起動する前に、環境変数 `GEMINI_API_KEY` または `GOOGLE_API_KEY` が設定されていること
- VSCode の組み込み Git 拡張が有効であること

## ライセンス

MIT License © 2025-2026 komiyamma
