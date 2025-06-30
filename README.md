# 模板仓库

## `config.json`

```json
{
  "pack_name": "minecraft-pack-template",
  "author": "XeKr-Dev",
  "description": "minecraft-pack-template",
  "version": "1.0.0",
  "base_path": "./src",
  "sets_path": "./sets",
  "icon": "./icon.png",
  "main_module": "main",
  "version_modules": {
    "1.21.1": {
      "module": "version_add_1",
      "strict": false
    }
  }
}
```

| 字段                | 类型                              | 描述                 |
|-------------------|---------------------------------|--------------------|
| pack_name         | string                          | 名称                 |
| author            | string                          | 作者                 |
| description       | string                          | 描述                 |
| version           | string                          | 版本                 |
| base_path         | string                          | 资源路径               |
| sets_path         | string?                         | 集合路径               |
| icon              | string?                         | 图标                 |
| type              | "resource"/"data"/undefined     | 类型                 |
| suggested_version | string?                         | 建议的 `Minecraft` 版本 |
| main_module       | string                          | 主模块                |
| version_modules   | {[key: string]: VersionModule}? | 版本模块               |

### `VersionModule`

| 字段     | 类型      | 描述       |
|--------|---------|----------|
| module | string  | 模块路径名称   |
| strict | boolean | 是否严格匹配版本 |

## `module.config.json`

```json
{
  "module_name": "minecraft-pack-template-module",
  "description": "测试用",
  "support_version": "*",
  "weight": 0,
  "breaks": [
    "add_3"
  ]
}
```

| 字段              | 类型      | 描述     |
|-----------------|---------|--------|
| module_name     | string  | 模块名称   |
| description     | string? | 模块描述   |
| support_version | string  | 支持的版本  |
| weight          | number  | 模块权重   |
| breaks          | array   | 不兼容的模块 |

## `*.set.config.json`

```json
{
  "set_name": "minecraft-pack-template-set-01",
  "description": "测试用01",
  "modules": [
    "add_1",
    "add_2",
    "add_3"
  ]
}
```

| 字段          | 类型      | 描述   |
|-------------|---------|------|
| set_name    | string  | 合集名称 |
| description | string? | 合集描述 |
| modules     | array   | 模块列表 |
