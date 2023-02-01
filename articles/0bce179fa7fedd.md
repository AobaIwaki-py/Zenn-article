---
title: "VSCodeで学習メモを快適に書く方法とストレスフリーでZennにアップロードする方法"
emoji: "💭"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["VSCode","Zenn","Tech"]
published: true
---
# はじめに
自分が学んだことを効率よく記事化して、ストレスフリーでZennにアップロードする方法について調べました。自分は、VSCode信者なので全てをVSCodeのみで完結させることにこだわりました。この記事では、便利な拡張機能の紹介を行います。詳細な使い方については参考元をご確認ください。

# 爆速でノートをとる方法
1. VSCodeの拡張機能VSNotesをインストールする。
`Command+Shift+P`
`VSNotes: Run setup`
を行い、ノートを保存するディレクトリを設定する。
2. VSCodeを起動します。この時、開くフォルダは上で指定したものでなくてもあまり問題ありません。
`Command+Shift+P`
`VSNotes:Create a New Note`
とすると、ファイル名を入力するフォームが現れます。この時、名前を選択しないとその時の日付と時刻が自動で入力されるので、面倒な場合は入力不要です。自分はほとんど入力していません。
3. あとは、マークダウン形式でメモをとるだけです。この時におすすめのGoogle Chromeの拡張機能は、[Copy as Markdown - Chrome Web Store](https://chrome.google.com/webstore/detail/copy-as-markdown/fkeaekngjflipcockcnpobkpbbfbhmdn)です。この拡張機能を使うと、開いているページのタイトルをマークダウン形式のリンクで取得できるので、参考記事としてそのまま貼り付けることができます。

# 書いた記事をVSCodeからZennへアップロードする方法
1. Zenn CLIのインストール

https://zenn.dev/zenn/articles/install-zenn-cli
2. ZennとGitHubの連携

https://zenn.dev/zenn/articles/connect-to-github
3. VSCodeの拡張機能Zen Editorのインストール

https://zenn.dev/negokaz/articles/aa4e12b76d516597a00e
4. 記事の作成
`Command+Shift+P`
`Zenn Editor: Create New Article`
この時、GitHubに同期しなくても良いファイルも生成されるので、`.gitignore`に`*.json`と`.keep`を追記してからコミットする。
5. あとは、すでに書いたマークダウンファイルを貼り付けるか、記事を執筆する。publishedをtrueにしてコミットおよびプッシュをすると自動的に公開される。非公開も同様に操作可能。但し、GitHub上のファイルを削除してもZenn上の記事は消えない。公開、非公開は、VSCode上及びZenn上の両方で可能。異なる設定をした場合、最後に反映したものが優先される。
# 参考記事
- [めんどくさがりでもできるVSCodeを使ったノートのとり方とドキュメント化について](https://zenn.dev/optimisuke/articles/9e60519d9a506699d701)
  - こちらは、あまりZennへのアップロードとは関係ありません。しかし、マークダウンでメモを作る際に便利な拡張機能が多く紹介されていたのでとても参考になりました。

# おすすめMacアプリケーション
- [Clipy/Clipy: Clipboard extension app for macOS.](https://github.com/Clipy/Clipy)
  - Macは、Windowsと異なり、クリップボードがありません。そのため、コピー履歴を遡れずとても不便です。そんなイライラを解消してくれるのがこのアプリです。

# さいごに
初めてZennの記事を書いたのでわかりづらい部分も多々あると思いますが、追記してほしいことがあればコメントで教えてくださると幸いです。