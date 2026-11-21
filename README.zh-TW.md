[English](README.md) | [簡體中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md)

# P6spy Spring Boot Starter

讓 Spring Boot 應用快速整合 p6spy 以列印 SQL 日誌。

## 快速開始

- 匯入相依性

```xml
    <dependency>
        <groupId>com.jiovan.spring.starter</groupId>
        <artifactId>p6spy-spring-boot-starter</artifactId>
        <version>LATEST</version>
    </dependency>
```

> 預設情況下，此 starter 會自動生效，你可以透過 `jiovan.p6spy.enabled = false` 關閉它。

- 使用字首 `jiovan.p6spy` 設定 Spring Boot 的 `application.yml`

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

## 文件

- GitHub：https://github.com/jiovan-labs/p6spy-spring-boot-starter
- P6Spy GitHub：https://github.com/p6spy/p6spy
- P6Spy 設定項：https://p6spy.readthedocs.io/en/latest/configandusage.html

## 環境要求

- jdk 17+

## 許可證

本專案採用 [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) 許可證。

請參閱 `NOTICE.txt` 檔案瞭解所需的宣告與歸屬資訊。

## 捐贈

喜歡這個工具包嗎？歡迎[向我們捐贈](https://jiovan.com/donation)以支援開發。

## 版權

北京玖漫科技有限公司

## 網站

- 玖漫：https://jiovan.com
