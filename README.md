# coding-principles

给 AI 编码代理（Claude Code、Codex）用的全局编码原则，浓缩自 [webpro/programming-principles](https://github.com/webpro/programming-principles)（commit `a0c299c`，2026-06-30）。原文没有的内容在文件里标为「（补充）」。

原文仓库没有声明许可证，所以这里不收录原文，只给链接。

## 用法

[coding-principles.md](coding-principles.md) 是原则正文，用作 Claude Code 的 `~/.claude/CLAUDE.md` 和 Codex 的 `~/.codex/AGENTS.md`。

Linux / macOS / WSL：

```bash
git clone https://github.com/cybergeek2077/coding-principles.git ~/coding-principles
ln -s ~/coding-principles/coding-principles.md ~/.claude/CLAUDE.md
ln -s ~/coding-principles/coding-principles.md ~/.codex/AGENTS.md
```

Windows（管理员 cmd，或开启开发者模式后用普通权限）：

```bat
mklink %USERPROFILE%\.claude\CLAUDE.md <克隆目录>\coding-principles.md
mklink %USERPROFILE%\.codex\AGENTS.md <克隆目录>\coding-principles.md
```

Claude Code 云端会话（claude.ai/code）不读本机的 `~/.claude/CLAUDE.md`，要在个人云环境的 setup script 里加：

```bash
mkdir -p ~/.claude && curl -fsSL https://raw.githubusercontent.com/cybergeek2077/coding-principles/main/coding-principles.md -o ~/.claude/CLAUDE.md
```
