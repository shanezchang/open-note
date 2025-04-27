# Python Log





| 级别                 | 数值 | 何种含义 / 何时使用                                          |
| :------------------- | :--- | :----------------------------------------------------------- |
| logging.**NOTSET**   | 0    | 当在日志记录器上设置时，表示将查询上级日志记录器以确定生效的级别。 如果仍被解析为 `NOTSET`，则会记录所有事件。 在处理器上设置时，所有事件都将被处理。 |
| logging.**DEBUG**    | 10   | 详细的信息，通常只有试图诊断问题的开发人员才会感兴趣。       |
| logging.**INFO**     | 20   | 确认程序按预期运行。                                         |
| logging.**WARNING**  | 30   | 表明发生了意外情况，或近期有可能发生问题（例如‘磁盘空间不足’）。 软件仍会按预期工作。 |
| logging.**ERROR**    | 40   | 由于严重的问题，程序的某些功能已经不能正常执行               |
| logging.**CRITICAL** | 50   | 严重的错误，表明程序已不能继续执行                           |



| 属性名称        | 格式                         | 描述                                                         |
| :-------------- | :--------------------------- | :----------------------------------------------------------- |
| args            | 此属性不需要用户进行格式化。 | 合并到 `msg` 以产生 `message` 的包含参数的元组，或是其中的值将被用于合并的字典（当只有一个参数且其类型为字典时）。 |
| asctime         | `%(asctime)s`                | 表示人类易读的 [`LogRecord`](https://docs.python.org/zh-cn/3/library/logging.html#logging.LogRecord) 生成时间。 默认形式为 '2003-07-08 16:49:45,896' （逗号之后的数字为时间的毫秒部分）。 |
| created         | `%(created)f`                | 当 [`LogRecord`](https://docs.python.org/zh-cn/3/library/logging.html#logging.LogRecord) 被创建的时间（即 [`time.time_ns()`](https://docs.python.org/zh-cn/3/library/time.html#time.time_ns) / 1e9 所返回的值）。 |
| exc_info        | 此属性不需要用户进行格式化。 | 异常元组（例如 `sys.exc_info`）或者如未发生异常则为 `None`。 |
| filename        | `%(filename)s`               | `pathname` 的文件名部分。                                    |
| funcName        | `%(funcName)s`               | 函数名包括调用日志记录.                                      |
| levelname       | `%(levelname)s`              | 消息文本记录级别（`'DEBUG'`，`'INFO'`，`'WARNING'`，`'ERROR'`，`'CRITICAL'`）。 |
| levelno         | `%(levelno)s`                | 消息数字的记录级别 ([`DEBUG`](https://docs.python.org/zh-cn/3/library/logging.html#logging.DEBUG), [`INFO`](https://docs.python.org/zh-cn/3/library/logging.html#logging.INFO), [`WARNING`](https://docs.python.org/zh-cn/3/library/logging.html#logging.WARNING), [`ERROR`](https://docs.python.org/zh-cn/3/library/logging.html#logging.ERROR), [`CRITICAL`](https://docs.python.org/zh-cn/3/library/logging.html#logging.CRITICAL)). |
| lineno          | `%(lineno)d`                 | 发出日志记录调用所在的源行号（如果可用）。                   |
| message         | `%(message)s`                | 记入日志的消息，即 `msg % args` 的结果。 这是在发起调用 [`Formatter.format()`](https://docs.python.org/zh-cn/3/library/logging.html#logging.Formatter.format) 时设置的。 |
| module          | `%(module)s`                 | 模块 (`filename` 的名称部分)。                               |
| msecs           | `%(msecs)d`                  | [`LogRecord`](https://docs.python.org/zh-cn/3/library/logging.html#logging.LogRecord) 被创建的时间的毫秒部分。 |
| msg             | 此属性不需要用户进行格式化。 | 在原始日志记录调用中传入的格式字符串。 与 `args` 合并以产生 `message`，或是一个任意对象 (参见 [使用任意对象作为消息](https://docs.python.org/zh-cn/3/howto/logging.html#arbitrary-object-messages))。 |
| name            | `%(name)s`                   | 用于记录调用的日志记录器名称。                               |
| pathname        | `%(pathname)s`               | 发出日志记录调用的源文件的完整路径名（如果可用）。           |
| process         | `%(process)d`                | 进程ID（如果可用）                                           |
| processName     | `%(processName)s`            | 进程名（如果可用）                                           |
| relativeCreated | `%(relativeCreated)d`        | 以毫秒数表示的 LogRecord 被创建的时间，即相对于 logging 模块被加载时间的差值。 |
| stack_info      | 此属性不需要用户进行格式化。 | 当前线程中从堆栈底部起向上直到包括日志记录调用并引发创建当前记录堆栈帧创建的堆栈帧信息（如果可用）。 |
| thread          | `%(thread)d`                 | 线程ID（如果可用）                                           |
| threadName      | `%(threadName)s`             | 线程名（如果可用）                                           |
| taskName        | `%(taskName)s`               | [`asyncio.Task`](https://docs.python.org/zh-cn/3/library/asyncio-task.html#asyncio.Task) 名称（如果可用）。 |

