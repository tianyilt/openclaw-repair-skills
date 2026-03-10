# openclaw-repair-skills

<div align="center">

[![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-OpenClaw%20%7C%20NanoClaw%20%7C%20Claude%20Code-orange?style=for-the-badge)](https://github.com/tianyilt/openclaw-repair-skills)
[![Skills](https://img.shields.io/badge/Skills-1-brightgreen?style=for-the-badge)](skills/)
[![ClawHub](https://img.shields.io/badge/ClawHub-lobster--doctor-red?style=for-the-badge)](https://clawhub.ai/skills/lobster-doctor)

**Open-source skills for diagnosing and fixing OpenClaw / NanoClaw problems.**

[English](#english) | [中文](#中文)

</div>

---

## English

### What Is This?

**openclaw-repair-skills** is a collection of AI agent skills focused on one thing: **fixing broken OpenClaw / NanoClaw setups**. Think of it as the lobster doctor — when your claw is broken, these skills know how to diagnose and repair it.

These skills are compatible with:

| Platform | How to use |
|----------|-----------|
| [OpenClaw](https://github.com/openclaw/openclaw) | Copy to `<workspace>/skills/` or `~/.openclaw/skills/` |
| [NanoClaw](https://github.com/MedClaw-Org) | Same as OpenClaw |
| [Claude Code](https://github.com/anthropics/claude-code) | Add trigger block to `~/.claude/CLAUDE.md` |

### Skills

| Skill | Description |
|-------|-------------|
| [lobster-doctor](skills/lobster-doctor/SKILL.md) | Diagnose and fix common OpenClaw issues: skill not triggering, script path errors, API key failures, missing dependencies, YAML frontmatter bugs, post-update breakage |

### Install

#### Via ClawHub (recommended)

```bash
clawhub install lobster-doctor
```

#### Manual (git clone)

```bash
git clone https://github.com/tianyilt/openclaw-repair-skills.git

# Workspace install (recommended, higher priority)
cp -r openclaw-repair-skills/skills/* <your-workspace>/skills/

# Global install (shared across all agents)
cp -r openclaw-repair-skills/skills/* ~/.openclaw/skills/
```

Skills are picked up automatically on the next session.

#### Claude Code

1. Copy the Claude Code trigger block from the bottom of [skills/lobster-doctor/SKILL.md](skills/lobster-doctor/SKILL.md)
2. Paste it into `~/.claude/CLAUDE.md` under `## User-Invocable Skills`
3. Invoke with `/lobster-doctor`

### Contributing

Found a new failure mode? Open a PR with:
1. Symptom (exact error or behavior)
2. Root cause
3. Diagnostic command
4. Fix

---

## 中文

### 这是什么？

**openclaw-repair-skills** 是一组专门用于诊断和修复 OpenClaw / NanoClaw 故障的 AI agent skill。

可以把它理解成**龙虾医生**——当你的爪子坏了，它来帮你修。

### 支持平台

| 平台 | 使用方式 |
|------|---------|
| [OpenClaw](https://github.com/openclaw/openclaw) | 复制到 `<workspace>/skills/` 或 `~/.openclaw/skills/` |
| [NanoClaw](https://github.com/MedClaw-Org) | 同 OpenClaw |
| [Claude Code](https://github.com/anthropics/claude-code) | 将触发块添加到 `~/.claude/CLAUDE.md` |

### Skill 列表

| Skill | 说明 |
|-------|------|
| [lobster-doctor](skills/lobster-doctor/SKILL.md) | 诊断并修复常见 OpenClaw 问题：skill 不触发、脚本路径错误、API key 未配置、依赖缺失、YAML 格式错误、更新后失效等 |

### 安装

#### 通过 ClawHub 安装（推荐）

```bash
clawhub install lobster-doctor
```

#### 手动安装（git clone）

```bash
git clone https://github.com/tianyilt/openclaw-repair-skills.git

# 工作区安装（推荐，优先级更高）
cp -r openclaw-repair-skills/skills/* <your-workspace>/skills/

# 全局安装（所有 agent 共享）
cp -r openclaw-repair-skills/skills/* ~/.openclaw/skills/
```

下次会话自动生效，无需重启。

#### Claude Code

1. 复制 [skills/lobster-doctor/SKILL.md](skills/lobster-doctor/SKILL.md) 末尾的 Claude Code 触发块
2. 粘贴到 `~/.claude/CLAUDE.md` 的 `## User-Invocable Skills` 下
3. 用 `/lobster-doctor` 调用

### 贡献

发现新的故障模式？欢迎提 PR，包含：
1. 症状（具体报错或现象）
2. 根因
3. 诊断命令
4. 修复方法

---

## Citation

If this project helps your research or workflow, please cite it:

```bibtex
@misc{openclaw-repair-skills,
  author       = {tianyilt},
  title        = {openclaw-repair-skills: Open-source skills for diagnosing and fixing OpenClaw / NanoClaw problems},
  year         = {2025},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/tianyilt/openclaw-repair-skills}},
}
```

---

## Acknowledgements

Skill format inspired by [OpenClaw Medical Skills](https://github.com/FreedomIntelligence/OpenClaw-Medical-Skills).

## License

MIT
