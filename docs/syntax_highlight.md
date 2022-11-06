# syntax highlight をいい感じにする

[nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter) というプラグインがある

## tree-sitter とは
[tree-sitter](https://github.com/tree-sitter/tree-sitter)

> Tree-sitter is a parser generator tool and an incremental parsing library. It can build a concrete syntax tree for a source file and efficiently update the syntax tree as the source file is edited.

## nvim-treesitter をインストールする

`~/.config/nvim/lua/plugins.lua` に以下のように行を追加する。

```lua
use { 'nvim-treesitter/nvim-treesitter', run = ':TSUpdate' }
```

この状態でとりあえず `:PackageCompile`, `:PackageInstall` しておくとよさそう

## 自動でパーサーをインストールする
以下の設定を `init.lua に書けばよさそう

```lua
require'nvim-treesitter.configs'.setup {
  ensure_installed = "maintained",
  highlight = {
    enable = true,
  },
}
```


