# Arya - a configurable mock server

### Project Components

* [arya-view](https://github.com/mongolian-navy/arya-view): mock服务配置前端工程
* [arya-admin](https://github.com/mongolian-navy/arya-admin): mock服务配置后端工程
* [arya-engine](https://github.com/mongolian-navy/arya-engine): mock服务运行引擎

### Arya Architecture

```

+--------+             +----------+             +----------+
|        |  edit conf  |          |             |          |
|        | +---------> |          |             |          |
|        |             |          | start/stop  |          |
|  view  |             |  admin   | +---------> |  engine  |
|        |             |          |   reload    |          |
|        | +---------> |          |             |          |
|        | start/stop  |          |             |          |
+--------+             +---+------+             +----------+
                           |
                           |  ^
                           v  |
                              |
                       +------+---+
                       |          |
                       |    DB    |
                       |          |
                       +----------+

```
