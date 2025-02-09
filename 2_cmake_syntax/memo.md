* メッセージバッファリングの仕組みがあるらしく、 `message` コマンドの出力が変わることがある
  * STATUSキーワードを与えると即座に出力されるらしい
    * 要出典
    * `message(STATUS "This is ...")`
  * cmake_print_variables のようなコマンドを使用するとこの問題が発生するよう
  