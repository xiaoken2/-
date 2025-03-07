# 1. 项目需求：
- 登录注册
- 游戏菜单
- 五子棋游戏
- 游戏后台展示

# 2. 项目背景
使用Muduo库构建的HTTP框架
- Muduo是一个C++11编写的开源网络库，它提供了一种简单、高效、可扩展的C++网络编程模型，并使用非阻塞I/O模型，以异步的方式处理网络请求。
-- Reactor架构
   1. Main Reactor 负责监听新的连接（accept），通过轮询方式将连接分发给Sub Reactor
   2. Sub Reactor 负责处理连接的读写事件，并通过轮询分发给Event Handler
-- 核心组件
   1. EventLoop：事件循环，用于处理IO事件，包括读写事件、定时事件等。
   2. Channel：封装了IO事件，包括文件描述符、事件类型、回调函数等。
   3. Poller：用于监听IO事件，包括epoll、kqueue等。
   4. Timer：用于处理定时事件，包括定时器、定时任务等。
   5. EventHandler：用于处理IO事件，包括连接建立、读写事件等。

# 3. 项目组件
  1. HttpRequest和HttpResponse：HttpRequest用于封装HTTP请求和响应，包括请求方法、请求路径、请求头、请求体等；HttpResponse管理HttpResponse的响应状态码、响应头、响应体等。
  2. HttpContext：用于封装HTTP请求在处理过程中的状态，跟踪解析状态并存储HttpRequest对象，确保请求的完整性和一致性。
  3. HttpServer：
  4. 路由和处理器：
  5. 日志记录和错误处理：
  6. 会话管理：
  7. 中间件：

# 4. 