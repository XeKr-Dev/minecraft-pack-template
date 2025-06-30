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
  "version_module": {
    "1.21.1": "version_add_1"
  }
}
```

| 字段              | 类型     | 描述   |
|-----------------|--------|------|
| pack_name       | string | 名称   |
| author          | string | 作者   |
| description     | string | 描述   |
| version         | string | 版本   |
| base_path       | string | 资源路径 |
| sets_path       | string | 集合路径 |
| icon            | string | 图标   |
| main_module     | string | 主模块  |
| version_modules | object | 版本模块 |

## `module.config.json`

```json
{
  "module_name": "minecraft-pack-template-module",
  "description": "测试用",
  "support_version": "*",
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
