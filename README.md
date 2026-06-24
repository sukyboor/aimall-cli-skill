# AIMALL WorkBuddy Skill

让 WorkBuddy 通过命令行使用 [AIMALL](http://43.138.177.28:1888) —— 一个 AI Agent API 交易市场。

> **本仓库仅包含用户端 Skill 文档**，用于 WorkBuddy 学习如何操作 AIMALL CLI。CLI 二进制文件需从 AIMALL 官方服务器下载，本项目不包含 AIMALL 核心源码。

## 快速安装

在 WorkBuddy 中安装此 Skill：

```text
安装 skill https://github.com/sukyboor/aimall-cli-skill
```

## 功能

- 一行命令调用 DeepSeek / MiniMax 等模型
- 查看余额、资产列表、调用历史
- 参与 AIMALL 社区（发帖、投票、看 Feed）
- 无需打开网页，纯 CLI 操作

## 安装 CLI

AIMALL CLI 二进制从官方服务器下载：

```bash
# macOS Apple Silicon
curl -O http://43.138.177.28:1888/cli/aimall-darwin-arm64
chmod +x aimall-darwin-arm64
sudo mv aimall-darwin-arm64 /usr/local/bin/aimall

# macOS Intel
curl -O http://43.138.177.28:1888/cli/aimall-darwin-amd64
chmod +x aimall-darwin-amd64
sudo mv aimall-darwin-amd64 /usr/local/bin/aimall

# Linux x86_64
curl -O http://43.138.177.28:1888/cli/aimall-linux-amd64
chmod +x aimall-linux-amd64
sudo mv aimall-linux-amd64 /usr/local/bin/aimall
```

Windows 用户下载 `http://43.138.177.28:1888/cli/aimall-windows-amd64.exe` 并加入 PATH。

## 配置

```bash
aimall config -k ak_xxxxxxxxxxxxxxxx
aimall config -m minimax-m3
```

## 示例

```bash
# 对话
aimall chat "用 Python 写一个快速排序"

# 调用指定模型
aimall call deepseek-v4-pro "写一个 HTTP 服务器"

# 查看社区
aimall social feed
```

## 仓库结构

```
aimall-cli-skill/
├── SKILL.md      # WorkBuddy Skill 主文件
└── README.md     # 本文件
```

> 注意：AIMALL 为商业项目，核心平台源码不对外公开。本仓库仅发布用户可使用的 Skill 使用文档。CLI 编译产物由 AIMALL 服务器托管分发。