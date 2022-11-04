# hachi neovim
hachi のための neovim の設定とドキュメント。
neovim 使ったり使わなかったりしていて設定や操作方法を忘れがちなのでドキュメントにしておきたいという気持ちがある。

[LunarVim](https://www.lunarvim.org/) を使っていた事もあったが、結局なにをどうしたらいいのかわからなくなったのでやめた。自分でゼロから構築する。

## ToC
[インストール](docs/setup.md)
[package manager をいれる](docs/install_package_manager.md)
markdown を書きやすくする


## FAQ


### クリップボードと共有したい
(ノーマルモード|ヴィジュアルモード)時に `"+` を使うことでクリップボードに共有できる。
```sh
# カレント行コピー
"+yy
```

cf. [Vimでクリップボードを使う](https://psipsina.jp/note/vim/neovim_clipboard.html)

### 画面を分けたい
水平分割 `:sp[lit]`
垂直分割 `:vs[plit]`

cf. https://neovim.io/doc/user/vimindex.html

### 分けた画面を移動したい
Window commands というくくりがあるっぽい。デフォルトの prefix は `CTRL-W`
cf. [Window commands](https://neovim.io/doc/user/vimindex.html#CTRL-W)

### neovim 内で terminal を使いたい
`:te[rminal]` でターミナルを開ける

### 


### [wip]buffer ってなんぞ
terminal command の説明に `open a terminal buffer` って書いてある。buffer ってなんぞや

### キーリピートがうまく使えない
どうやら iterm2 を使っていると発生する問題らしい。つらい。
cf. [macOS Mojaveのキーリピートで困った話](https://blog.nijohando.jp/post/mojave-key-repeat-problem/)



## 資料集
[neovim.io](https://neovim.io/)
[Commands Index](https://neovim.io/doc/user/vimindex.html)







