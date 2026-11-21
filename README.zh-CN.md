[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md)

# P6spy Spring Boot Starter

让 Spring Boot 应用快速集成 p6spy 以打印 SQL 日志。

## 快速开始

- 导入依赖

```xml
    <dependency>
        <groupId>com.jiovan.spring.starter</groupId>
        <artifactId>p6spy-spring-boot-starter</artifactId>
        <version>LATEST</version>
    </dependency>
```

> 默认情况下，此 starter 会自动生效，你可以通过 `jiovan.p6spy.enabled = false` 关闭它。

- 使用前缀 `jiovan.p6spy` 配置 Spring Boot 的 `application.yml`

```yml
spring:
    datasource:
        url: 'jdbc:p6spy:mysql://xxx'
        driver-class-name: com.jiovan.revival.p6spy.engine.spy.P6SpyDriver
jiovan:
    p6spy:
        appender: com.jiovan.revival.p6spy.engine.spy.appender.Slf4JLogger
        log-message-format: com.jiovan.revival.p6spy.engine.spy.appender.CompactLineFormat
        reload-properties: false
```

## 文档

- GitHub：https://github.com/jiovan-labs/p6spy-spring-boot-starter
- P6Spy GitHub：https://github.com/p6spy/p6spy
- P6Spy 配置项：https://p6spy.readthedocs.io/en/latest/configandusage.html

## 环境要求

- jdk 17+

## 许可证

本项目采用 [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) 许可证。

请参阅 `NOTICE.txt` 文件了解所需的声明与归属信息。

## 捐赠

喜欢这个工具包吗？欢迎[向我们捐赠](https://jiovan.com/donation)以支持开发。

## 版权

北京玖漫科技有限公司

## 网站

- 玖漫：https://jiovan.com
