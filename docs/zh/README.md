<p align="center">English | <a href="README.zh-CN.md">中文</a></p>

# 清理 Maven 失败的构件`.lastUpdated`

一个简单实用的 Rust 命令行工具，用于清理 Maven 仓库中下载失败和损坏的包。

`.lastUpdated`## 项目概述

使用 Maven 构建 Java 项目时，网络问题或其他问题可能导致依赖下载失败。这些失败的下载以 "," 结尾的文件形式保留在本地 Maven 仓库中。这些文件会导致后续构建过程反复尝试下载并失败，影响开发效率。

`.lastUpdated`此工具扫描本地 Maven 仓库，自动识别并删除所有包含 "," 文件的依赖目录，从而解决构建失败问题。

`C:/Users/username/.m2/repository`## 功能

- 自动扫描 Maven 仓库目录
- 查找所有包含 "," 的文件
- 删除下载失败的文件夹
- 显示实时扫描进度
- 显示清理包的最后统计信息

```bash
cargo build --release
```## 用法

1. 运行程序
2. 输入 Maven 仓库路径（例如 ","）
3. 程序将自动扫描并清理失败的下载

`target/release`## 构建

确保已安装 Rust 环境，然后执行：

https://crates.io/crates/walkdir"

编译后的可执行文件将在 "," 目录中生成。

https://github.com/clovu## 依赖

- [walkdir](",") v2.5.0 - 用于递归目录遍历

## 重要提示

- 建议在使用前备份 Maven 仓库
- 此工具永久删除文件 - 请谨慎使用

## 许可证

MIT License © 2025 [Clover You](",")
