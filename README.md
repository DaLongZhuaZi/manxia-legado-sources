# 漫匣 Legado 书源索引模板

[English](README.en.md)

这是漫匣用于 Legado 兼容书源同步机制的索引格式模板。

## 重要声明

漫匣 App 与本仓库不提供、不内置、不推荐、不托管、不维护任何书源。

用户需要自行导入、创建或维护 Legado 书源。本仓库默认保持空索引，只用于说明格式、验证同步流程，以及为用户自管仓库提供参考结构。

## 应用默认读取地址

```text
https://raw.githubusercontent.com/DaLongZhuaZi/manxia-legado-sources/master/index.main.json
```

默认索引为空，因此不会向用户下发任何书源。

## 目录结构

```text
index.main.json
<pkg>/source.json
<pkg>/icon.webp
```

每个书源条目在 `index.main.json` 中注册，并指向一个独立的 `<pkg>` 目录。`source.json` 必须是漫匣能够导入的 Legado 兼容书源 JSON。

## 索引格式

```json
{
  "schemaVersion": "1.0.0",
  "repositoryName": "ManXia Legado Source Index Template",
  "lastUpdate": 0,
  "sources": []
}
```

书源条目字段固定为：

```json
{
  "pkg": "com.example.source",
  "name": "Example Source",
  "bookSourceUrl": "https://example.com",
  "bookSourceType": 0,
  "lang": "zh",
  "code": 1,
  "version": "1.0.0",
  "nsfw": 0,
  "hasIcon": false,
  "sourcePath": "com.example.source/source.json",
  "sha256": "<source.json sha256>",
  "minAppVersionCode": 0,
  "minRuntimeApi": 1,
  "changelog": ""
}
```

更新 `<pkg>/source.json` 后，必须同步更新对应条目的 `sha256`、`code`、`version` 和 `changelog`。

## 使用建议

用户或社区可以 fork 本仓库作为个人索引仓库，但需要自行承担书源来源、可用性、合法性与维护责任。

漫匣只校验索引结构、文件路径、大小和 `sha256`，不会背书任何第三方书源内容。

