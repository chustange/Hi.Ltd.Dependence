# 依赖文件目录说明

本目录用于存放程序运行所需的环境依赖文件，按平台分类存放。

## 目录结构

```
dependencies/
├── windows/   # Windows 平台依赖文件
├── linux/     # Linux 平台依赖文件
├── macos/     # macOS 平台依赖文件
└── common/    # 跨平台通用依赖文件
```

## 下载说明

您可以通过以下方式下载所需的依赖文件：

### 方式一：通过 GitHub Releases 下载（推荐）

访问 [Releases 页面](https://github.com/chustange/Hi.Ltd.Dependence/releases) 下载对应版本的依赖包。

### 方式二：直接下载单个文件

在对应平台目录中找到所需文件，点击文件名后使用 GitHub 的 **Raw** 或 **Download** 按钮下载。

### 方式三：克隆仓库

```bash
git clone https://github.com/chustange/Hi.Ltd.Dependence.git
```

## 使用方法

1. 根据您的操作系统，进入对应目录（`windows`、`linux` 或 `macos`）。
2. 下载所需文件到您的程序目录。
3. 通用依赖文件位于 `common` 目录，所有平台均需下载。
