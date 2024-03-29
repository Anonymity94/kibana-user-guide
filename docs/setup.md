# 搭建
> 原文：[https://www.elastic.co/guide/en/kibana/current/setup.html](https://www.elastic.co/guide/en/kibana/current/setup.html)

本章节将介绍如何搭建并运行 Kibana，包含如下内容：
- 下载
- 安装
- 启动
- 配置
- 升级

## 支持的平台编辑
Kibana 有 Linux、Darwin 和 Windows 版本的安装包。由于 Kibana 基于 Node.js 运行，我们在这些平台上包含了一些必要的 Node.js 二进制文件。Kibana 不支持在独立维护的 Node.js 版本上运行。

## Elasticsearch 版本
Kibana 的版本需要和 Elasticsearch 的版本一致。这是官方支持的配置。

运行不同主版本号的 Kibana 和 Elasticsearch 是不支持的（例如 Kibana 5.x 和 Elasticsearch 2.x），若主版本号相同，运行 Kibana 子版本号比 Elasticsearch 子版本号新的版本也是不支持的（例如 Kibana 5.1 和 Elasticsearch 5.0）。

运行一个 Elasticsearch 子版本号大于 Kibana 的版本基本不会有问题，这种情况一般是便于先将 Elasticsearch 升级（例如 Kibana 5.0 和 Elasticsearch 5.1）。在这种配置下，Kibana 启动日志中会出现一个警告，所以一般只是使用于 Kibana 即将要升级到和 Elasticsearch 相同版本的场景。

运行不同的 Kibana 和 Elasticsearch 补丁版本一般是支持的（例如：Kibana 5.0.0 和 Elasticsearch 5.0.1），尽管我们鼓励用户去运行最新的补丁更新版本。