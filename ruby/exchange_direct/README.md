exchange 的 direct 模式通过 routing_key 的完全匹配来确定向那些 queue 发送信息

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_direct.png)

在窗口运行 `ruby receive_logs_direct.rb warning error` 来订阅 routing_key 是 warning 或者 error 的信息
在窗口运行 `ruby receive_logs_direct.rb info warning error` 来订阅 routing_key 是 info, warning 或者 error 的信息
在第三个新窗口运行 `ruby emit_log_direct.rb error "Run. Run. Or it will explode."` 来发送一个 routing_key 为 error 的信息

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_direct_demo.png)