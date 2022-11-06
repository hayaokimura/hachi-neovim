# buffers とは？、tabpage, window とは？

ここでは、 buffers, tabpage, window などのエディタ表示領域についての話を記述する

A buffer is the in-memory text of a file.
A window is a viewport on a buffer.
A tab page is a collection of windows.

らしい。

## buffer
`:buffers` で buffer を見ることができる。試しに `:vs` でwindow を分けてみる

buffer は `active`, `hidden`, `inactive` の３つの state を持つ。

## 資料
[neovim.io#windows](https://neovim.io/doc/user/windows.html#windows)



