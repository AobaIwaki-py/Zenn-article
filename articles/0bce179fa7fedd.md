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
2. ZennとGitHubの連携
3. VSCodeの拡張機能Zen Editorのインストール
4. 記事の作成
`Command+Shift+P`
`Zenn Editor: Create New Article`
この時、GitHubに同期しなくても良いファイルも生成されるので、`.gitignore`に`*.json`と`.keep`を追記してからコミットする。
5. あとは、すでに書いたマークダウンファイルを貼り付けるか、記事を執筆する。publishedをtrueにしてコミットおよびプッシュをすると自動的に公開される。非公開も同様に操作可能。但し、GitHub上のファイルを削除してもZenn上の記事は消えない。公開、非公開は、VSCode上及びZenn上の両方で可能。異なる設定をした場合、最後に反映したものが優先される。
# 参考記事一覧
- [めんどくさがりでもできるVSCodeを使ったノートのとり方とドキュメント化について](https://zenn.dev/optimisuke/articles/9e60519d9a506699d701)
  - こちらは、あまりZennへのアップロードとは関係ありません。しかし、マークダウンでメモを作る際に便利な拡張機能が多く紹介されていたのでとても参考になりました。
- [Zenn の執筆を支援する VSCode 拡張 Zenn Editor](https://zenn.dev/negokaz/articles/aa4e12b76d516597a00e)
  - VSCode上でZennにアップロードした時のプレビューをできる拡張機能についての紹介記事です。VSCodeでZennの記事を書きたいなら必読です。
- [Zenn CLIをインストールする](https://zenn.dev/zenn/articles/install-zenn-cli)
  - Zenn Editorを使うには、Zenn CLIのインストールが必要です。そのための手順がまとめられています。Node.jsを使ったことがない場合はそれも必要になります。[Node.jsのインストール](https://nodejs.org/ja/)
- [GitHubリポジトリでZennのコンテンツを管理する](https://zenn.dev/zenn/articles/connect-to-github)
  - ローカルの変更をオンライン上に橋渡しするためにZennとGitHubを連携する必要があります。そのための手順がまとめられています。
# おすすめGoogle Chrome 拡張機能
- [Copy as Markdown - Chrome Web Store](https://chrome.google.com/webstore/detail/copy-as-markdown/fkeaekngjflipcockcnpobkpbbfbhmdn)
  - リンクをマークダウン形式でコピーできます.貼り付けるだけでリンクになるので非常に便利です。自分は、`Command+Shift+C`でできるようにしています。

# おすすめVS Code拡張機能
- [VSNotes - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=patricklee.vsnotes)
  - `Command+Shift+P`と`VSNotes:Create a new note`で指定のディレクトリに自動でマークダウンファイルを生成してくれます。面倒臭ければ、ファイル名を指定する必要もありません。非常に快適です。
- [Zenn Editor - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=negokaz.zenn-editor)
  - Zennの記事をVSCodeで快適に書くための拡張機能です。
- [Paste Image - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image)
  - Zennの記事を書く際には、画像の管理が別なので使えませんが普通にマークダウンに画像をコピペしたい時に非常に便利です。


# おすすめMacアプリケーション
- [Clipy/Clipy: Clipboard extension app for macOS.](https://github.com/Clipy/Clipy)
  - Macは、Windowsと異なり、クリップボードがありません。そのため、コピー履歴を遡れずとても不便です。そんなイライラを解消してくれるのがこのアプリです。

# さいごに
初めてZennの記事を書いたのでわかりづらい部分も多々あると思いますが、追記してほしいことがあればコメントで教えてくださると幸いです。