* メッセージバッファリングの仕組みがあるらしく、 `message` コマンドの出力が変わることがある
  * STATUSキーワードを与えると即座に出力されるらしい
    * 要出典
    * `message(STATUS "This is ...")`
  * cmake_print_variables のようなコマンドを使用するとこの問題が発生するよう

* 存在しない変数を参照した時にエラーとしたり警告を出したりする機能はcmakeにない
  * このような関数で変数の存在チェックをできる
  * ```
    function(check_defined var_name)
      if(NOT DEFINED ${var_name})
          message(FATAL_ERROR "Variable '${var_name}' is not defined")
      endif()
    endfunction()
    ```