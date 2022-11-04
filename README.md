# hachi neovim
hachi のための neovim の設定とドキュメント。
neovim 使ったり使わなかったりしていて設定や操作方法を忘れがちなのでドキュメントにしておきたいという気持ちがある。

[LunarVim](https://www.lunarvim.org/) を使っていた事もあったが、結局なにをどうしたらいいのかわからなくなったのでやめた。自分でゼロから構築する。

## ToC
[インストール](docs/setup.md)
[neovim に設定を追加する](docs/add_configuration_to_neovim.md)
[package manager をいれる](docs/install_package_manager.md)
markdown を書きやすくする
- markdown のファイル名にカーソルを合わせて、なにかしたらそのファイルを作成して開いてほしい
- なんか見出しの色が薄くて辛いのでもうちょっといい色ないかな
- 入力補助してほしい
- タグっぽいものを使えるようにしたい

- vimコマンドのヒストリーが見たいしヒストリー補完できると嬉しい
- 下の、コマンド入れられたり、現在の状態が書いてあったりするバーってどういう名前なのか知りたい
- というか各エリアの名前があるなら知りたい
- `CTRL-C` で日本語入力を解除したい。
- カーソルを合わせているURLをゴニョゴニョすると chrome で開いてほしい


## FAQ

### カーソル移動を文字種類単位で行いたい
`f[word]` で次の文字へ `F[word]` で前の文字へ移動


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

cf. [](https://thata.hatenadiary.org/entry/20100606/1275796513)

## 資料集
[neovim.io](https://neovim.io/)
[Commands Index](https://neovim.io/doc/user/vimindex.html)







