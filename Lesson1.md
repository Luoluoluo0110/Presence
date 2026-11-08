# Lesson 1：模拟面试与问题整理

## 模拟面试

### 通用问题

1. 自我介绍。
2. 分别介绍项目和技术的优势。
3. 在项目中介绍你负责的部分。
4. 项目采用新方案后 Token 消耗下降 55%，这个结果是如何获得的？
5. 自我介绍书面版（1.5 分钟以内）。
6. 八股问题的理解与理解性背诵。

### Python 相关

1. Python 的 GIL（全局解释器锁）是什么？
2. 多线程、多进程和异步 I/O 的区别；了解五种 I/O 模型。
3. 如果项目同时调用墨迹天气、高德地图和 QQ 音乐，应采用异步 I/O 还是多进程？
4. FastAPI 中 `async def` 和 `def` 的区别是什么？前者一定更快吗？请举例说明。
5. 项目中调用同步、阻塞的 SDK 时怎么办？
6. Python 中浅拷贝和深拷贝的区别。
7. Python 装饰器及其使用场景。

### 数据库与缓存相关

1. 数据库已更新但 Redis 仍返回旧数据，如何解释和解决？（Cache-Aside）
2. HTTP 中 GET 和 POST 接口的区别。
3. MySQL 索引如何工作？为什么使用 B+ 树？
4. 为什么使用 Redis？
5. Redis 数据一定不会丢失吗？什么时候会丢失？
6. 数据库事务：讲一下 ACID。

### AI 基础相关

1. RAG 是什么？什么时候使用 RAG？
2. 讲一下 Embedding。
3. Function Calling 和 MCP 的区别。
4. LoRA 和全参数微调有什么区别？

### 部署与运维相关

1. Docker、镜像和容器的区别。
2. 删除容器后，相关数据仍会保留吗？
3. RESTful API 是什么？
4. HTTP 常用状态码有哪些？
5. CI/CD 是什么？是否用过？
6. 新版本错误率上升，如何排查和解决？
7. 线上工具调用率下降，如何排查和解决？

### 手撕题

实现异步工具工厂：最多三个任务并发、每个任务两秒超时；单个任务失败不能导致其他任务丢失；返回结果顺序应与输入顺序一致。

```python
import asyncio
from typing import Any, Awaitable, Callable


async def execute_tools(
    tasks: list[Callable[[], Awaitable[Any]]],
    max_concurrency: int = 3,
    timeout: float = 2.0,
) -> list[dict]:
    # 请完成代码
    pass
```
