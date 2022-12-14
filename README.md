# hachi neovim
hachi のための neovim の設定とドキュメント。
neovim 使ったり使わなかったりしていて設定や操作方法を忘れがちなのでドキュメントにしておきたいという気持ちがある。

[LunarVim](https://www.lunarvim.org/) を使っていた事もあったが、結局なにをどうしたらいいのかわからなくなったのでやめた。自分でゼロから構築する。

## 疑問に思っていること
- textobject ってなんぞや
https://zenn.dev/yutakatay/articles/neovim-plugins-2022#treesitter-textobj-%26-operator

- [zk-nvim](https://github.com/mickael-menu/zk-nvim) がメモ取るのにめっちゃ使えそう
- markdown のファイル名にカーソルを合わせて、なにかしたらそのファイルを作成して開いてほしい

## ToC
[インストール](docs/setup.md)

[neovim に設定を追加する](docs/add_configuration_to_neovim.md)

[package manager をいれる](docs/install_package_manager.md)

[syntax highlight をいい感じにする](docs/syntax_highlight.md)

[buffers とは？](docs/what-is-buffers.md)

wip: [LSP を使う](docs/use-lsp.md)
- 入力補助してほしい

markdown を書きやすくする
- タグっぽいものを使えるようにしたい
- telescope 見た目もそうだけどもう少し使い勝手を良くしたい cf. [telescope.nvim の記事](https://dev.classmethod.jp/articles/nvim_telescope/)
- git をいい感じに扱えるようにしたい

- 下の、コマンド入れられたり、現在の状態が書いてあったりするバーってどういう名前なのか知りたい
- というか各エリアの名前があるなら知りたい
- `CTRL-C` で日本語入力を解除したい。
- いい感じにファイル名を表示してほしい。色とか、ディレクトリ省略とか
- git で管理しているリポジトリトップから表示してほしい
- いい感じにchrome からコピーしてきたURLをタイトル入れて markdown リンク化してほしい(これは chrome の責務かもしれない)
- ヒストリー補完できると嬉しい
  - ddc.vim というのがどうやらあるらしい
  - cf. [新世代の自動補完プラグイン ddc.vim](https://zenn.dev/shougo/articles/ddc-vim-beta)

- config に簡単に飛びたい
  - telescope の global に飛べるやつが使えるかも？

## FAQ

### vimコマンドのヒストリーが見たい
`q:`と入力すると見れる。

### markdown のリンクに飛びたい
[follow-md-links.nvim](https://github.com/jghauser/follow-md-links.nvim) を使うと、リンクに Enter で飛べるようになる。

### Leader key の設定
leader key は \ にデフォルトでは設定されているので、space に設定し直した。
以下のように書くと設定できる。

```lua
vim.g.mapleader = " "
```

cf. [Neovim プラグインをほぼ全て Lua に移行した](https://zenn.dev/acro5piano/articles/c764669236eb0f)


### `CTRL-C`で日本語入力を解除したい
ESCだと簡単
cf. https://blog.pepo-le.com/vim-normalmode-imeoff/#:~:text=%E3%82%BF%E3%83%BC%E3%83%9F%E3%83%8A%E3%83%AB%E4%B8%8A%E3%81%AEVim%E3%81%AF,%E3%81%8C%E7%84%A1%E5%8A%B9%E3%81%AB%E3%81%AA%E3%82%8A%E3%81%BE%E3%81%99%E3%80%82



### カーソル移動を文字種類単位で行いたい
`f[word]` で次の文字へ `F[word]` で前の文字へ移動


### クリップボードと共有したい
(ノーマルモード|ヴィジュアルモード)時に `"+` を使うことでクリップボードに共有できる。
```sh
# カレント行コピー
"+yy
```

cf. [Vimでクリップボードを使う](https://psipsina.jp/note/vim/neovim_clipboard.html)
### neovim 内で terminal を使いたい
`:te[rminal]` でターミナルを開ける
そのままではノーマルモードなので、`i`で入力できる。
`CTRL-\ + CTRL-N` でノーマルモードに戻れる。


### [wip]buffer ってなんぞ
terminal command の説明に `open a terminal buffer` って書いてある。buffer ってなんぞや

### キーリピートがうまく使えない
どうやら iterm2 を使っていると発生する問題らしい。つらい。
cf. [macOS Mojaveのキーリピートで困った話](https://blog.nijohando.jp/post/mojave-key-repeat-problem/)


### 折返しのときに、`j`や`k`で移動すると次の行に行ってしまわず、ビジュアル的に同じ行だと扱ってほしい

```vimrc
"カーソルを表示行で移動する。物理行移動は<C-n>,<C-p>
nnoremap j gj
nnoremap k gk
nnoremap <Down> gj
nnoremap <Up>   gk
```

cf. [s](https://thata.hatenadiary.org/entry/20100606/1275796513)

### telescope を使ったとき、どのディレクトリ配下としてみなしている？
current directory という概念が vim には存在していて、その配下を検索している。

cf. [neovim.io#current-directory](https://neovim.io/doc/user/editing.html#current-directory)


## 資料集
[neovim.io](https://neovim.io/)
[Commands Index](https://neovim.io/doc/user/vimindex.html)







