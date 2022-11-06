# package manager をインストールする

## 知りたいこと
start ディレクトリまで作る必要あったのか？

## vim の packages 機能
packpath というものが存在していて、そこに package を置くと読み込んでくれるらしい。
packpath の設定値は `:set packpath?` でみられる。

cf. [おすすめプラグイン 〜 Vimはいいぞ！ゴリラと学ぶVim講座(7)](https://knowledge.sakura.ad.jp/23248/)


## Packer.nvim のインストール
自分は Package Manager に Packer.nvim を使おうと思ったので使う。とりあえず Packer.nvim の [Quickstart](https://github.com/wbthomason/packer.nvim#quickstart) に従ってみる。

```sh
git clone --depth 1 https://github.com/wbthomason/packer.nvim\
 ~/.local/share/nvim/site/pack/packer/start/packer.nvim
```

start ディレクトリまで作る必要あったのか？

とりあえず、`~/.config/nvim/lua/plugins.lua` に設定を書くといいっぽいのでかく。公式は結構ボリュームある設定ファイルになってる

```lua
-- This file can be loaded by calling `lua require('plugins')` from your init.vim

-- Only required if you have packer configured as `opt`
vim.cmd [[packadd packer.nvim]]

return require('packer').startup(function(use)
  -- Packer can manage itself
  use 'wbthomason/packer.nvim'

end)
```

`~/.config/nvim/init.lua` に、以下の行を追加して、`:PackerCompile`, `:PackerInstall` command を打つと neovim に反映される

