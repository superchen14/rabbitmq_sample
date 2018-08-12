一个 queue 可以有多个 consumer

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/work_queues.png)

在两个窗口运行 `ruby worker.rb`
在第三个新窗口运行
```
ruby new_task.rb First message.
ruby new_task.rb Second message..
ruby new_task.rb Third message...
```

![](https://raw.githubusercontent.com/superchen14/rabbitmq_sample/master/img/work_queues_demo.png)