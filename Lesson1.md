# Lesson1

____

### 模拟面试和相关问题整理

#### 1.模拟面试

##### 通用问题

自我介绍

分别介绍项目和技术的优势

在这个项目里面介绍你负责的部分

项目里使用新方案token下降55%，结果是如何获得的

##### python相关

python语言的GIL(全局解释锁)是啥

多线程，多进程，异步IO三者区别 -> 五种IO模式

如果项目同时调用墨迹天气，高德地图，qq音乐，是采用异步io还是多进程

fast-api 中的async def和def区别，是否前者一定比后者更快，举出相应的例子？

项目中调用同步阻塞的SDK，怎么办

##### 数据库相关

数据库已经更新但是redis仍然返回旧的数据，如何解释和解决（Cash-Aside）

python中的浅拷贝和深拷贝区别

python的装饰器和使用的场景

http中的GET，POST接口区别

MySQl的索引是如何工作的，为啥使用B+tree这个数据结构

Redis为啥这模块

Redis的数据一定不会丢失吗，什么时候会丢失

数据库的事务，讲一下ACID

##### AI相关基础问题

RAG是啥，什么时候要使用RAG

讲一下embedding

function calling 和 MCP的区别

Lora和全参数的微调有啥区别

##### 部署相关问题

docker和镜像和容器有啥区别

删除这个容器，相关数据仍然会保留吗

RESTful api是什么

HTTP常用状态码分别是啥

CICD是啥，有用过吗

新版本错误率上升，如何排查和解决

线上工具调用率下降，如何排查和解决

##### 手撕相关

异步工厂，三个并发，两秒超时，三个任务失败，不能导致其他任务丢失，返回的结果顺序和输入顺序一致

```
import asyncio
from typing import Awaitable, Callable, Any

async def execute_tools(
    tasks: list[Callable[[], Awaitable[Any]]],
    max_concurrency: int = 3,
    timeout: float = 2.0,
) -> list[dict]:
    # 请完成代码
    pass
```

自我介绍书面版（1.5min之内）

八股问题理解和理解性背诵

