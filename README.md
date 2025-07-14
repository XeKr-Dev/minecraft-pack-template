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
  "file_mode": false,
  "version_modules": {
    "version_add_1": {
      "version": "1.21.1",
      "strict": false,
      "target": "main"
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
| license           | string?                         | 开源协议，默认为 `ARR`     |
| main_module       | string                          | 主模块                |
| file_mode         | boolean?                        | 是否启用从文件构建          |
| version_modules   | {[key: string]: VersionModule}? | 版本模块               |

### `VersionModule`

| 字段      | 类型      | 描述                 |
|---------|---------|--------------------|
| version | string  | 匹配的 `Minecraft` 版本 |
| strict  | boolean | 是否严格匹配版本           |
| target  | string? | 要覆盖的模块，默认为主模块      |

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
