# setup
[Install from download](https://github.com/neovim/neovim/wiki/Installing-Neovim#install-from-download)に従う。

ネットでは homebrew を使う方法が一般的だが、聞くところによると homebrew でインストールできる neovim のバージョンが結構古いのでダウンロードして自分でインストールしたほうが良いらしい。

今の最新は [0.8.0](https://github.com/neovim/neovim/releases/tag/v0.8.0) なのでそれを入れる。
macOS のインストールガイドがあるのでそれに従う。

```sh
$ xattr -c ./Downloads/nvim-macos.tar.gz
$ tar xzvf ./Downloads/nvim-macos.tar.gz
```

で一瞬で使えるようになった。どこに置くか悩んだけど、`.nvim` ディレクトリを作成してそこに置くことにした。

```sh
$ mv nvim-macos .nvim
```

パス通したらあとはもう使える。

```zshrc
export PATH="$HOME/.nvim/bin:$PATH"
```



