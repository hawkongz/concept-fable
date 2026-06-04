<div align="center">
  <h1>📖 概念寓言（Concept Fable）</h1>
  <p>用一篇精心设计的寓言故事，让你在恍然大悟中理解任何抽象概念——而非死记硬背教科书定义。</p>

  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)
  [![Platform](https://img.shields.io/badge/Platform-Claude%20Code-blue)](https://code.claude.com)
  [![Stars](https://img.shields.io/github/stars/hawkongz/concept-fable)](https://github.com/hawkongz/concept-fable)

  <p><strong>Language:</strong> <a href="../README.md">English</a> | <a href="README.md">简体中文</a></p>
  <p><strong>作者</strong> <a href="https://github.com/hawkongz">@hawkongz</a> 与 Claude 共同创作</p>
</div>

---

## 📋 目录

- [背景：来自 Amanda Askell 的灵感](#背景来自-amanda-askell-的灵感)
- [这个 Skill 做了什么](#这个-skill-做了什么)
- [特性](#特性)
- [快速开始](#快速开始)
- [使用示例](#使用示例)
- [设计理念](#设计理念)
- [相关话题](#相关话题)
- [贡献](#贡献)
- [许可证](#许可证)

---

## 背景：来自 Amanda Askell 的灵感

**Amanda Askell** 是 Anthropic 的驻场哲学家、Claude 性格对齐团队负责人。她拥有纽约大学哲学博士学位，主导编写了长达三万字的「Claude 宪法」——那套塑造 Claude 性格与道德准则的核心文档。

2025 年 4 月，Askell 在一次播客访谈中分享了一个小方法，却在中文 AI 社区引发了广泛传播：

> **"让 Claude 写一篇寓言故事来解释一个概念——但全程不准出现这个概念的名字。"**

她的核心洞见很简单，却极为深刻：

> *"故事是人类最根本的学习载体。传统学习方式是直接啃概念和定义，而寓言故事走的是完全相反的路——你先沉浸在一个引人入胜的故事里，读到结尾才恍然大悟：原来讲的是这个。此时概念的核心本质你早已在故事中'悟'到了。"*

Askell 自己这样用："我无聊时就让 Claude 讲寓言故事，后来脑子里装了好多小故事，每个故事对应一个学科概念。有时候我已经记不住概念的学名了，但那个故事还记得。"

**这个 Skill 正是从她的想法出发，将一则简单的 Prompt 扩展为一套完整、结构化、可复用的方法论。**

---

## 这个 Skill 做了什么

Askell 的原版思路是一个绝妙的起点，但实际使用中会遇到几个问题：

- AI 容易陷入套路化叙事（旅人寻求智慧、村庄顿悟、智者对话……）
- 意象反复撞车（河流、钟表、群山、回声城……）
- 角色常常沦为概念的「提线木偶」，为隐喻牺牲了故事的自然感
- 隐喻载体有时比概念本身更抽象（用修仙体系解释设计模式……）

**概念寓言 Skill** 将 Askell 的核心理念系统化为 **7 步工作流**，并加入了大量防套路、保质量的机制：

| Askell 原版思路 | 本 Skill 的系统化扩展 |
|:---|:---|
| 不出现概念名 | Step 4：三段式结构，精确控制揭晓时机 |
| 让故事承载意义 | Step 4：因果链贴合检查——情节的「因→果→困境」必须复现概念的运作机制 |
| — | Step 3：根据概念特征自动选择故事类型（博弈→古代寓言 / 渐进→日常生活 / 涌现→自然或机械） |
| — | Step 3：根据概念情感色彩匹配叙事语气（告诫 / 反直觉 / 权衡 / 机制） |
| — | Step 6：7 条自检——角色自然度、隐喻准确性、故事独立性、揭晓时机、简洁度、具象化、术语闭环 |
| — | 反模式表：6 种常见失败模式及修正方法 |
| — | 隐喻具象化原则（「奶奶测试」）：载体必须是日常可感知的事物 |
| — | 降级策略：概念不适合寓言形式时的 4 种替代方案 |

---

## 特性

- **📚 7 步结构化工作流**：理解概念 → 确认场景 → 选择类型与语气 → 写故事 → 附释义 → 自检 → 输出
- **🎭 故事类型自动匹配**：根据概念的核心特征（博弈/渐进/涌现/反差），自动选择最合适的寓言类型
- **🎯 因果链贴合检查**：不是只碰「主题」，而是确保故事情节的因果链条精准映射概念的运作机制
- **🧹 反套路机制**：内置角色傀儡化、隐喻过度、揭晓过早等 6 种反模式的黑名单和自动规避
- **👵 奶奶测试**：硬性要求隐喻载体必须是日常可感知的事物（做饭、开车、排队），禁用需要解码的抽象设定
- **✅ 7 条质量自检**：写完后逐条审视，最多重写 2 次，不通过则诚实告知
- **🔄 反馈处理闭环**：隐喻不准、故事不好、太隐晦/太直白、太长/太短——每种反馈都有对应的调整策略
- **📖 专业释义模板**：统一的释义输出格式，包含定义、故事对应表、前置知识说明、延伸思考

---

## 快速开始

> **你需要什么：** 安装了 Claude Code 的终端环境。

**Step 1 — 安装 Skill**

本 Skill 仅需一个 `SKILL.md` 文件即可运行（中文版）。

macOS / Linux：

```bash
mkdir -p ~/.claude/skills/concept-fable
curl -o ~/.claude/skills/concept-fable/SKILL.md https://raw.githubusercontent.com/hawkongz/concept-fable/main/zh-CN/SKILL.md
```

Windows（PowerShell）：

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\concept-fable"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/hawkongz/concept-fable/main/zh-CN/SKILL.md" -OutFile "$env:USERPROFILE\.claude\skills\concept-fable\SKILL.md"
```

**Step 2 — 完成**

重启 Claude Code，Skill 自动生效。试试这样说：

- 「用故事解释一下死锁」
- 「CAP 定理是什么意思？讲个寓言吧」
- 「帮我理解依赖注入，用日常场景」

> 更新：重新执行 Step 1 的命令即可。

---

## 使用示例

**输入：**「用故事解释什么是死锁」

**Claude 会：**
1. 确认概念理解（死锁的四个必要条件、核心矛盾）
2. 选择故事类型（两方博弈 → 古代寓言风格）
3. 创作一篇不出现「死锁」二字的寓言
4. 在故事结尾揭晓概念
5. 附上专业释义和故事元素对应表
6. 自检后输出

故事可能是：两辆马车在窄桥上对峙，谁也不肯退让，直到天黑双方都困在原地——而桥下明明有足够的空间让其中一辆先过。

---

## 设计理念

### 核心原则：用故事让人「悟到」，而不是用定义让人「记住」

传统教学走的是「定义 → 解释 → 举例」的路径，读者是被动接受者。

寓言方法走的是相反的路：「故事 → 沉浸 → 顿悟 → 揭晓」。读者在不知道自己在「学什么」的情况下，已经理解了概念的核心理念。揭晓的那一刻，产生的是「原来讲的是这个」的恍然大悟——这种情感锚定让记忆远比被动接受深刻。

### 为什么有效

1. **叙事记忆优势**：人类大脑对故事的记忆远强于对抽象定义的记忆。故事提供了情境、情感和因果链条。
2. **先悟后知**：读者在故事中已经在理解概念，只是不知道它的学名。揭晓时产生的「顿悟感」比被告知强烈得多。
3. **降低认知门槛**：用日常场景映射抽象概念，读者不需要先啃完教科书才能理解。

---

## 相关话题

[`claude-code`](https://github.com/topics/claude-code) [`skill`](https://github.com/topics/skill) [`prompt-engineering`](https://github.com/topics/prompt-engineering) [`fable`](https://github.com/topics/fable) [`storytelling`](https://github.com/topics/storytelling) [`education`](https://github.com/topics/education) [`learning`](https://github.com/topics/learning) [`concept-explanation`](https://github.com/topics/concept-explanation)

---

## 贡献

欢迎提出改进建议！如果你有更好的故事类型、发现了新的反模式、或者有特别成功的寓言案例，请提交 Issue 或 PR。

---

## 许可证

MIT © [hawkongz](https://github.com/hawkongz)

---

> *"有时候我已经记不住概念的学名了，但那个故事还记得。"* —— Amanda Askell
