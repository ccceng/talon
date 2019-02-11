# talon
talon是一个mini http web服务器，目前只实现了GET方法，使用Linux C开发，操作系统Ubuntu。
## 目的
- 学习网络并发编程
- 学习Linux系统编程
- C语言实践

## 特点
- 主进程 + 工作进程，主进程创建工作进程后就sleep。
- 工作进程负责处理http请求，每个工作进程独自accept，accept之前要获得锁，工作进程之间使用文件加锁同步。
- I/O事件使用epoll。
- 服务器可配置。

## 使用
> `$ cd talon`

> `$ make`

> `$ ./talon`
