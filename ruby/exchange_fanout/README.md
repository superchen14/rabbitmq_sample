exchange 是 rabbitmq 中的重要概念，producer 应该向 exchange 发送信息
exchange 决定如何向绑定他的 queue 发送信息
exchange 的 fanout 模式向所有绑定它的 queue 发送信息

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_fanout.png)

在两个窗口运行 `ruby receive_logs.rb`
在第三个新窗口运行 `ruby emit_log.rb`

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_fanout_demo.png)