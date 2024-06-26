# mule-ops-benchmark-app

## test-ops-benchmark-001-app の実行結果
* for-eachでループするよりも、DataWeaveでループするほうが早い。100回以上その傾向が現れ、1000回以上は顕著。

|count|for-each/set-payload|for-each/set-var|for-each/tran-msg|dw/set-payload|
|-:|-:|-:|-:|-:|
|1|       1|   2|   8| 3|
|10|      6|   2|   2| 1|
|100|    38|   7|   9| 1|
|1000|  110|  23|  52| 2|
|10000| 328| 129| 349| 5|
|100000|947|1070|2611|15|

* CPU AMD Ryzen 7 3700X 8-Core Processor 3.60 GHz
* MEM 32GB
* OS Windows 11 Pro 23H2
* Mule Runtime Version: 4.4.0-20220824 Build: 37ce7934
* Server started: 2024/06/27 1:33
* JDK: 1.8.0_345 (mixed mode)
