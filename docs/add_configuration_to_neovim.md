# neovim に設定を追加する

`.config/nvim/init.lua` に設定を書く。

今まで、 vim script を使ってた印象なんだけど、最近は lua script を使うらしい。

例えば、行番号を追加したいなら、`vim.opt.number = true` を追加する。

cf. [Getting started using Lua in Neovim](https://github.com/willelz/nvim-lua-guide-ja/blob/master/README.ja.md#vim%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99%E3%82%8B)

## 設定を反映する
基本的には、 nvim コマンドを再起動すれば反映される。
また、一回`.config/nvim/init.lua` を作成して、`nvim` コマンドを呼ぶと、`$MYVIMRC` にパスが代入されるので、`:e $MYVIMRC` で設定ファイルを編集できるし、`:source $MYVIMRC` とすると、neovim を閉じなくても設定が反映される。（`set number` を消して更新しても反映されなかった気がするが気のせいか？）



