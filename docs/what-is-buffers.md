# buffers とは？、tabpage, window とは？

ここでは、 buffers, tabpage, window などのエディタ表示領域についての話を記述する

A buffer is the in-memory text of a file.
A window is a viewport on a buffer.
A tab page is a collection of windows.

らしい。

## buffer
`:buffers` で buffer を見ることができる。試しに `:vs` でwindow を分けてみる

buffer は `active`, `hidden`, `inactive` の３つの state を持つ。

## tabpage
tab は新しいページを作成できるっぽい。
`:tabnew` command が使える。
`:tabc[lose]` でタブを閉じれる
`:tabn[ext]` で次のタブ
`:tabo[nly]` で開いてるタブ以外閉じる

## window

### 画面を分けたい
水平分割 `:sp[lit]`
垂直分割 `:vs[plit]`

cf. https://neovim.io/doc/user/vimindex.html

### 分けた画面を移動したい
Window commands というくくりがあるっぽい。デフォルトの prefix は `CTRL-W`
cf. [Window commands](https://neovim.io/doc/user/vimindex.html#CTRL-W)



## 資料
[neovim.io#windows](https://neovim.io/doc/user/windows.html#windows)



