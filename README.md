# PUA-Web-Refactor Skill — Web 重构增强版

> **Make your AI dare not slack off. PUA Skill deeply optimized for Web architecture refactoring scenarios.**  
> **让 AI 不敢摆烂的 PUA Skill，针对 Web 架构重构场景深度优化。**  
> **Fork from [tanweai/pua](https://github.com/tanweai/pua)**

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Chinese](https://img.shields.io/badge/language-中文-red.svg)](README_zh.md)
[![English](https://img.shields.io/badge/language-English-green.svg)](#-quick-start)

---

## 🎯 这是什么？What's This?

这是一个**让 AI 编程助手不敢摆烂、不敢空口完成、不敢被动等待**的 Skill 插件。

This is a **PUA (Pick-up Artist) Skill plugin that makes AI programming assistants dare not slack off, dare not claim completion without verification, dare not wait passively**.

适用于：
Suitable for:
- ✅ **Web 前端架构重构**（如移除预处理阶段、迁移框架）
  **Web frontend architecture refactoring** (e.g., removing preprocessing stages, migrating frameworks)
- ✅ **多文件联动修改**（改了 JS 需要联动 HTML/CSS）
  **Multi-file联动 modifications** (changed JS needs to sync HTML/CSS)
- ✅ **前后端接口对齐**（API 变更后前端适配）
  **Frontend-backend API alignment** (frontend adaptation after API changes)
- ✅ **大规模代码迁移**（变量命名统一、函数重组）
  **Large-scale code migration** (unified variable naming, function refactoring)
- ✅ **所有通用场景**（Debug、性能优化、写作等）
  **All general scenarios** (Debug, performance optimization, writing, etc.)

### 核心改进 Core Improvements

相比原版本，增加了以下**Web 重构特有功能**：

Compared to the original version, added these **Web refactoring specific features**:

#### 1️⃣ 铁律四：稳健第一 | Iron Rule 4: Stability First
```
改了 JS 必须检查 HTML/CSS，改了一个文件必须搜索所有引用处。
不允许出现"改了这头忘了那头"的低级错误。
```

#### 2️⃣ Lingma 特供版·稳健 Rule（5 条具体规则） | Lingma Special · Robust Rules (5 Concrete Rules)
- ✅ **先搜后改**：修改任何变量/函数前，必须用 `grep_code` 搜索所有引用位置
- ✅ **同步更新**：发现同名变量在不同文件中，必须全部同步修改，不允许遗漏
- ✅ **HTML 联动**：改了 JS 中的 ID/class 名，必须检查 HTML 是否需要同步更新
- ✅ **CSS 联动**：改了 HTML 结构，必须检查 CSS 选择器是否需要调整
- ✅ **API 联动**：改了后端 API 的返回结构，必须检查前端调用处是否适配

#### 3️⃣ 新增失败模式检测 | New: Failure Mode Detection
| 失败模式 | 检测信号 | PUA 风味 |
|---------|---------|---------|
| 🔗 **Web 重构遗漏** | 改了 JS 忘 HTML/CSS、多文件引用不同步、前后端接口不对齐 | 🟠 阿里味·关怀型 → 🔴 华为味 → 🟢 腾讯味+⚫ 百度味 |

---

## 📦 快速开始 Quick Start

### 方式一：直接使用（推荐） | Method 1: Direct Use (Recommended)

本 skill 已放置在项目的 `.lingma/skills/pua-web-refactor/` 目录下，AI 会自动识别。

This skill is already placed in the project's `.lingma/skills/pua-web-refactor/` directory, AI will automatically recognize it.

**中文版**：
```
请使用 pua-web-refactor skill，我需要进行 Web 架构重构。
```

**英文版**：
```
Please use pua-web-refactor-en skill, I need Web architecture refactoring.
```

或者直接在复杂重构任务中说：
```
我要重构前端代码，启用稳健模式。
```

### 方式二：手动激活 | Method 2: Manual Activation

在任何对话中，你可以要求：

In any conversation, you can request:
```
/skill pua-web-refactor
```

---

## 💡 效果对比 Effect Comparison

### 原版 PUA（通用场景） | Original PUA (General Scenarios)
```
用户：帮我重构这个前端模块
AI：好的，已完成。（只改了 JS，没管 HTML/CSS）
用户：炸了！页面打不开了！
```

### PUA-Web-Refactor（Web 重构增强） | PUA-Web-Refactor (Web Refactoring Enhanced)
```
用户：帮我重构这个前端模块，启用 pua-web-refactor
AI：好的，开始重构...
   1. grep_code 搜索所有引用位置 ✓
   2. 同步更新 JS/HTML/CSS ✓
   3. 验证所有修改点 ✓
   4. 运行页面测试 ✓
   已完成，所有联动已检查，测试结果正常。
```

---

## 📊 与原版的区别 | Comparison with Original

| 功能模块 | 原版 (pua) | 增强版 (pua-web-refactor) |
|---------|-----------|-----------------|
| **核心铁律** | 3 条 | 4 条（+ 稳健第一） |
| **鞭策话术** | 通用 10 条 | 通用 10 条 + Web 专用 2 条 |
| **检查清单** | 主动出击 7 项 | 主动出击 10 项（+3 项 Web 专用） |
| **稳健规则** | 通用 5 步法 | 通用 5 步法 + Lingma 特供 5 条 |
| **抗合理化表** | 19 条 | 21 条（+2 条 Web 专用） |
| **失败模式** | 7 种 | 8 种（+Web 重构遗漏） |
| **适用场景** | 全场景通用 | 全场景 + Web 重构特化 |

---

## 🚀 使用场景 | Usage Scenarios

### 场景 1：防止 AI 摆烂 | Scenario 1: Prevent AI Slacking
```
我这个 bug 修了 3 次还没好，启用 pua-web-refactor skill。
```

### 场景 2：Web 重构防遗漏 | Scenario 2: Prevent Web Refactoring Omissions
```
我要移除预处理阶段，JS/HTML/CSS 都要改，用 pua-web-refactor 的稳健模式。
```

### 场景 3：多文件同步 | Scenario 3: Multi-file Synchronization
```
这个变量名要统一修改，整个项目有 5 个文件引用，用 pua-web-refactor 确保不遗漏。
```

---

## 📝 示例对话 | Example Dialogues

### 示例：AI 空口完成时 | Example: AI Claims Completion Without Verification
```
AI：已修复，请测试。
你：[自动触发] → 🟠 阿里味·验证型启动
AI：你说修复了——证据呢？build 跑了吗？页面打开了吗？
    curl 测试接口了吗？把输出贴上来。没有证据的修复不是修复，是自嗨。
    （然后自己跑去执行验证命令）
```

### 示例：AI 改了 JS 忘 HTML | Example: AI Changed JS Forgot HTML
```
AI：已重构 frontVideo/topVideo 变量。
你：[自动触发] → 🟠 阿里味·关怀型启动
AI：等等，你改了 JS 里的变量名，HTML 里的 id 检查了吗？
    grep_code 搜索其他引用处了吗？CSS 选择器对得上吗？
    这是 Web 重构的基本功，你居然会漏？
    （然后主动去检查 HTML 和 CSS）
```

---

## 🛡️ 稳健性检查清单（完整） | Robustness Checklist (Complete)

每次 Web 重构任务完成后，AI 必须自检：

After each Web refactoring task completion, AI must self-check:

- [ ] 修复是否经过验证？（运行测试、实际打开页面）
- [ ] 改了 JS？HTML 联动了吗？CSS 联动了吗？
- [ ] 同文件/同模块是否有类似问题？
- [ ] 上下游依赖是否受影响？
- [ ] 是否有边界情况没覆盖？
- [ ] 是否有更好的方案被我忽略了？
- [ ] 如果用户没有明确说的部分，我是否主动补充了？
- [ ] **【Web 专用】** 改了 JS 中的 ID/class/函数名，是否检查了 HTML 和 CSS？
- [ ] **【Web 专用】** 这个变量/函数在其他文件中是否有引用？grep_code 搜了吗？
- [ ] **【Web 专用】** 前后端接口变更，前端调用处是否全部同步更新？

---

## 🏗️ 项目结构 | Project Structure

```
pua-web-refactor-skill/
├── .lingma/
│   └── skills/
│       ├── pua-web-refactor/      # 中文版 Chinese version
│       │   ├── SKILL.md
│       │   └── README.md
│       └── pua-web-refactor-en/   # 英文版 English version
│           ├── SKILL.md
│           └── README.md
├── README.md                       # 项目说明 Project documentation
└── LICENSE                        # MIT License
```

---

## 📚 参考资料 | References

- 原项目：https://github.com/tanweai/pua
- Lingma 文档：https://lingma.aliyun.com/

---

## ⚖️ License

MIT License

---

## 🙏 致谢 | Acknowledgments

- 感谢 [tanweai/pua](https://github.com/tanweai/pua) 提供的优秀基础版本
- 感谢所有贡献者的大厂智慧

---

**Made with ❤️ by Fork from tanweai/pua**
