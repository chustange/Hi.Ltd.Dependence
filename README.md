# Hi.Ltd.Dependence

用于存放程序运行时的必要文件

## 目录结构

```
dependencies/
├── manifest.json       # 依赖清单（包含所有文件的下载地址）
├── windows/            # Windows 平台依赖文件
├── linux/              # Linux 平台依赖文件
├── macos/              # macOS 平台依赖文件
└── common/             # 跨平台通用依赖文件
```

## 下载地址

所有依赖文件均可通过以下基础地址直接下载：

```
https://github.com/chustange/Hi.Ltd.Dependence/raw/main/dependencies/
```

### 示例

| 平台 | 下载地址示例 |
|------|-------------|
| Windows | `https://github.com/chustange/Hi.Ltd.Dependence/raw/main/dependencies/windows/<文件名>` |
| Linux | `https://github.com/chustange/Hi.Ltd.Dependence/raw/main/dependencies/linux/<文件名>` |
| macOS | `https://github.com/chustange/Hi.Ltd.Dependence/raw/main/dependencies/macos/<文件名>` |
| 通用 | `https://github.com/chustange/Hi.Ltd.Dependence/raw/main/dependencies/common/<文件名>` |

## 依赖清单

完整依赖列表请参阅 [`dependencies/manifest.json`](./dependencies/manifest.json)。

## 如何使用

1. 查阅 `dependencies/manifest.json` 获取所需依赖文件的名称与版本
2. 根据运行平台，从对应目录下载文件
3. 将文件放置到程序指定的依赖目录中

## 如何添加新依赖

1. 将依赖文件上传到对应平台目录（`windows/`、`linux/`、`macos/` 或 `common/`）
2. 更新 `dependencies/manifest.json`，在 `dependencies` 数组中新增一条记录，格式如下：

```json
{
  "name": "your-dependency-name",
  "version": "1.0.0",
  "platform": "windows",
  "file_path": "windows/your-file.dll",
  "sha256": "<文件的 SHA-256 校验值>",
  "description": "依赖文件的说明"
}
```

| 字段 | 必填 | 说明 |
|------|------|------|
| `name` | ✅ | 依赖文件名称 |
| `version` | ✅ | 版本号，格式如 `1.0.0` |
| `platform` | ✅ | 适用平台：`windows` / `linux` / `macos` / `common` |
| `file_path` | ✅ | 相对于 `base_url` 的文件路径 |
| `sha256` | 推荐 | 文件 SHA-256 校验值，用于完整性验证 |
| `description` | ❌ | 文件说明（可选） |
