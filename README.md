# ManXia Legado Sources

Official Legado book source repository for ManXia.

The application reads:

```text
https://raw.githubusercontent.com/DaLongZhuaZi/manxia-legado-sources/master/index.main.json
```

## Layout

```text
index.main.json
<pkg>/source.json
<pkg>/icon.webp
```

Each source entry in `index.main.json` points to one package directory.
`source.json` must be a valid Legado book source JSON file accepted by ManXia.

## Index Fields

```json
{
  "schemaVersion": "1.0.0",
  "repositoryName": "ManXia Legado Sources",
  "lastUpdate": 0,
  "sources": []
}
```

For each source, update `sha256` after changing `<pkg>/source.json`.

