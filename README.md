# runes_log
关于runes符文的一些知识记录

# mint部分

- 解码内容
  // https://mempool.space/zh/tx/fd78d3edb63da303857acd1ebb37b31bf211bcecbf06e7a866de44244187d31f
  最简单的转移方式，直接转移符文对应的UTXO

  ```
  // https://mempool.space/zh/tx/fd78d3edb63da303857acd1ebb37b31bf211bcecbf06e7a866de44244187d31f
  {"edicts":[{"id":{"block":"840000","tx":"1"},"amount":"1900","output":"1"}]}
  ```
  表示转移数量1900

  ```
  // https://mempool.space/tx/ac1ae84d70f8dc847f7d6d08bcbfbd26ecb5adcba63f1081afab74253fecd34a
  {"edicts":[],"mint":{"block":"840000","tx":"1"},"pointer":"0"}
  ```
  表示转移数量为1，并且将符文放在交易的第一个输出上面

  ```
  // https://mempool.space/tx/0462d4a3ae59d6f5d7f20ad0fd19279eb79c3db6c918385007a4efceb73f5d74
  {"edicts":[],"mint":{"block":"840000","tx":"1"}}
  ```
  表示MINT数量为1，并且将符文放在交易的第一个脚本不需要OP_RETURN的输出中

