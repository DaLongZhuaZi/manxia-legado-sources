# ManXia Legado Source Index Template

[中文](README.md)

This repository is an empty index template for ManXia's Legado-compatible source sync mechanism.

## Important Notice

The ManXia app and this repository do not provide, bundle, recommend, host, or maintain any book source.

Users must import, create, or maintain their own Legado sources. This repository intentionally keeps an empty index. It only documents the manifest format, validates the sync flow, and provides a reference layout for user-managed repositories.

## Default App URL

```text
https://raw.githubusercontent.com/DaLongZhuaZi/manxia-legado-sources/master/index.main.json
```

The default index is empty, so it does not distribute any book source to users.

## Layout

```text
index.main.json
<pkg>/source.json
<pkg>/icon.webp
```

Each source entry is registered in `index.main.json` and points to a dedicated `<pkg>` directory. `source.json` must be a Legado-compatible source JSON that ManXia can import.

## Index Format

```json
{
  "schemaVersion": "1.0.0",
  "repositoryName": "ManXia Legado Source Index Template",
  "lastUpdate": 0,
  "sources": []
}
```

Each source entry uses the fixed fields below:

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

After changing `<pkg>/source.json`, update the entry's `sha256`, `code`, `version`, and `changelog`.

## Usage Notes

Users or communities may fork this repository as a personal index repository, but they are responsible for the source origin, availability, legality, and maintenance.

ManXia only validates index structure, file paths, file sizes, and `sha256`. It does not endorse any third-party source content.

