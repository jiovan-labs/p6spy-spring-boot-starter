# P6spy Spring Boot Starter

Spring Boot application integrates p6spy print SQL logs quickly.

## Quickstart

- Import dependencies

```xml
    <dependency>
        <groupId>com.jiovan.spring.starter</groupId>
        <artifactId>p6spy-spring-boot-starter</artifactId>
        <version>LATEST</version>
    </dependency>
```

> By default, this starter will auto take effect, you can turn it off by `jiovan.p6spy.enabled = false`

- Configure Spring Boot `application.yml` with prefix `jiovan.p6spy`

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

## Document

- Github: https://github.com/jiovan-labs/p6spy-spring-boot-starter
- P6spy github: https://github.com/p6spy/p6spy
- P6spy configurations: https://p6spy.readthedocs.io/en/latest/configandusage.html

## Requirement

- jdk 17+

## License

This project is under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)

See the `NOTICE.txt` file for required notices and attributions.

## Donation

You like this package? Then [donate to us](https://jiovan.com/donation) to support the development.

## Copyright

Beijing Jiovan Technology Ltd.

## Website

- Jiovan: https://jiovan.com
