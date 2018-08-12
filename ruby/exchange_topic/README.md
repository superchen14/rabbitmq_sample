exchange 的 topic 模式通过 routing_key 的模式匹配来确定向那些 queue 发送信息

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_topic.png)

在窗口运行 `ruby receive_logs_topic.rb "#"` 来订阅所有 log 信息
在窗口运行 `ruby receive_logs_topic.rb "kern.*"` 来订阅 kern 相关的 log 信息
在窗口运行 `ruby receive_logs_topic.rb "*.critical"` 来订阅 critical 相关的 log 信息
在窗口运行 `ruby receive_logs_topic.rb "kern.*" "*.critical"` 来订阅 kern 以及critical 相关的 log 信息
在窗口运行 `ruby emit_log_topic.rb "kern.critical" "A critical kernel error"` 来发送一个信息
![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/exchange_topic_demo.png)