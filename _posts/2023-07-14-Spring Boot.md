---
layout: post
title: Spring Boot
tags: [Spring Boot,Web Design]
---

# 1. 前置作業(好像有jdk就行)
1. 安裝 IntelliJ IDEA Community
   不要安裝最新版 安裝2019.3左右的(https://www.jetbrains.com/idea/download/other.html#2020.2)
    進入 IntelliJ 的 File>Settings>Build,Execution,Deployment>Build Tools>Gradle，並將Gradle JVM更改為 17
2. 安裝 Lombok plugin(https://plugins.jetbrains.com/plugin/6317-lombok)
3. 安裝 Pebble plugin(https://plugins.jetbrains.com/plugin/9407-pebble)
4. 安裝jdk(https://adoptopenjdk.net/)
   可以不設定JAVA_HOME

# 2. 架構
```
└── %project-root%
        ├── %project-child1%
        │   └── src\main
        │       ├── java\com\example\domo
        │       │   ├── bind
        │       │   ├── configuration
        │       │   ├── controller
        │       │   ├── service
        │       │   └── [MainApplication].java
        │       └── resources
        │           ├── application.yml
        │           ├── logback-spring.xml
        │           ├── java
        │           └── templates
        ├── build.gradle
        ├── lombok.config
        └── settings.gradle
```

## %project%/build.gradle
| 屬性               | 解釋                 |
| ------------------ | -------------------- |
| implementation     | 編譯，執行時使用     |
| testImplementation | 編譯，執行Test時使用 |
| runtimeOnly        | 執行時使用           |
	

# 開始
從 https://start.spring.io/ 建立專案
(?在依賴項增加 Lombok 和 web)

# 運行
set JAVA_HOME=C:\Program Files\Eclipse Adoptium\jdk-17.0.7.7-hotspot\
.\gradlew.bat id-manage:bootRun