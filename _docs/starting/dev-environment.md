---
title: Setting up a Development Environment
permalink: /docs/starting/platform
stable: 0.10.2
snapshot: SNAPSHOT
---

# Setting up a Development Environment

The JDK used is critical.  The latest stable release ({{page.stable}}) currently runs on JDK 21 and the {{page.snapshot}} on JDK 22.
Repository is optimised for Gradle development on Windows, targeting desktop and web.  It should work out of the box with the correct JDK.

```xml
<dependencies>
    <dependency>
        <groupId>com.littlekt</groupId>
        <artifactId>core</artifactId>
        <version>{{page.stable}}</version>
    </dependency>
    
    <dependency>
        <groupId>com.littlekt</groupId>
        <artifactId>scene-graph</artifactId>
        <version>{{page.stable}}</version>
    </dependency>
    
    <dependency>
        <groupId>org.jetbrains.kotlinx</groupId>
        <artifactId>kotlinx-coroutines-core</artifactId>
        <version>1.9.0</version>
    </dependency>
</dependencies>
```

# Other Platforms

Some platforms need a little more tweaking to get the build running.

## Desktop

For desktop, you're going to want to use `core-jvm` rather than `core`

```xml
<dependency>
    <groupId>com.littlekt</groupId>
    <artifactId>core-jvm</artifactId>
    <version>{{page.stable}}</version>
    <scope>compile</scope>
</dependency>
```

## MacOS

For MacOS you'll need some additional VM arguments

```
    --enable-preview -XstartOnFirstThread
```

