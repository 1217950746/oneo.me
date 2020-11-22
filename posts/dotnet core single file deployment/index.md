---
title: '.Net Core 单文件部署'
date: 2020-10-31 17:44
---

## 不可用 API

| API                          | 返回值                             |
| ---------------------------- | ---------------------------------- |
| Assembly.Location            | 空字符串                           |
| Module.FullyQualifiedName    | \<Unknown> 字符串，或引发异常      |
| Module.Name                  | \<Unknown> 字符串                  |
| Assembly.GetFile             | 引发 IOException                   |
| Assembly.GetFiles            | 引发 IOException                   |
| Assembly.CodeBase            | 引发 PlatformNotSupportedException |
| Assembly.EscapedCodeBase     | 引发 PlatformNotSupportedException |
| AssemblyName.CodeBase        | null                               |
| AssemblyName.EscapedCodeBase | null                               |

## 项目文件

```xml
<Project>
    <PropertyGroup>
        <!-- 使用 AppHost，false 不会生成可执行文件 -->
        <UseAppHost>true</UseAppHost>
        <!-- 设置目标 -->
        <RuntimeIdentifier>win10-x64</RuntimeIdentifier>
        <!-- 设置单文件 -->
        <PublishSingleFile>true</PublishSingleFile>
        <!-- 设置不依赖框架 -->
        <SelfContained>true</SelfContained>
        <!-- 裁剪输出程序集 -->
        <PublishTrimmed>true</PublishTrimmed>
        <!-- 嵌入 PDB -->
        <DebugType>embedded</DebugType>
    </PropertyGroup>
</Project>
```

## 命令行调用

单文件无依赖程序

```bash
dotnet publish -r win-x64 -p:PublishSingleFile=true --self-contained true
```

单文件框架依赖

```bash
dotnet publish -r win-x64 -p:PublishSingleFile=true
```
