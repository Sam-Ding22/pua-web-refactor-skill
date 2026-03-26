# PUA-Web-Refactor Skill — Web Refactoring Enhanced

> **Make your AI dare not slack off. PUA Skill deeply optimized for Web architecture refactoring scenarios.**  
> **Fork from [tanweai/pua](https://github.com/tanweai/pua)**

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

---

## 🎯 What's This?

This is a **PUA (Pick-up Artist) Skill plugin that makes AI programming assistants dare not slack off, dare not claim completion without verification, dare not wait passively**.

Suitable for:
- ✅ **Web frontend architecture refactoring** (e.g., removing preprocessing stages, migrating frameworks)
- ✅ **Multi-file联动 modifications** (changed JS needs to sync HTML/CSS)
- ✅ **Frontend-backend API alignment** (frontend adaptation after API changes)
- ✅ **Large-scale code migration** (unified variable naming, function refactoring)
- ✅ **All general scenarios** (Debug, performance optimization, writing, etc.)

### Core Improvements

Compared to the original version, added these **Web refactoring specific features**:

#### 1️⃣ Iron Rule 4: Stability First
```
When changing JS, must check HTML/CSS.
When modifying one file, must search all references.
No rookie mistakes like "fixed this end, forgot that end".
```

#### 2️⃣ Lingma Special · Robust Rules (5 Concrete Rules)
- ✅ **Search First**: Before changing any variable/function, must use `grep_code` to search all references
- ✅ **Sync Update**: When finding same variable name in different files, must sync update all, no omissions
- ✅ **HTML Linkage**: Changed JS ID/class names, must check if HTML needs sync update
- ✅ **CSS Linkage**: Changed HTML structure, must check if CSS selectors need adjustment
- ✅ **API Linkage**: Changed backend API return structure, must check frontend calls for adaptation

#### 3️⃣ New Failure Mode Detection
| Failure Mode | Detection Signal | PUA Flavor |
|-------------|------------------|------------|
| 🔗 **Web Refactoring Omission** | Changed JS forgot HTML/CSS, multi-file desync, frontend-backend misalignment | 🟠 Alibaba · Care → 🔴 Huawei · Wolf → 🟢 Tencent + ⚫ Baidu |

---

## 📦 Quick Start

### Method 1: Direct Use (Recommended)

This skill is already placed in the project's `.lingma/skills/pua-web-refactor-en/` directory, AI will automatically recognize it.

Tell AI at the beginning of the conversation:
```
Please use pua-web-refactor-en skill, I need Web architecture refactoring.
```

Or directly in complex refactoring tasks:
```
I need to refactor frontend code, enable robust mode.
```

### Method 2: Manual Activation

In any conversation, you can request:
```
/skill pua-web-refactor-en
```

---

## 🎯 When to Use

### ✅ Applicable Scenarios

- **Architecture Refactoring**: Removing preprocessing stages, migrating frameworks (React → Vue, etc.)
- **Multi-file Modifications**: Changing variables/functions that require sync updates across multiple files
- **Frontend-Backend Alignment**: Backend API changes, frontend needs adaptation
- **Bug Fixes**: Especially repeated bugs, same issue occurs multiple times
- **Performance Optimization**: Need to proactively search for optimization opportunities
- **Code Review**: Need to comprehensively check code quality, security, performance

### ❌ Not Recommended

- **Simple Q&A**: Already clear requirements, just need implementation
- **Emergency Fixes**: Need quick fixes first, optimization later
- **Exploratory Tasks**: Requirements unclear, need user interaction to clarify

---

## 💡 Usage Examples

### Example 1: Web Architecture Refactoring

**User**:
```
I need to remove the preprocessing stage, directly use API calls.
There are 5 files involved, please use pua-web-refactor-en.
```

**AI Will**:
1. ✅ Search all references to preprocessing stage
2. ✅ Check JS/HTML/CSS sync modifications
3. ✅ Verify API calls work correctly
4. ✅ Proactively check if similar preprocessing exists elsewhere

### Example 2: Repeated Bug Fixes

**User**:
```
This bug has been fixed 3 times and still not working, enable pua-web-refactor-en skill.
```

**AI Will**:
1. ✅ Check root cause (not just patch)
2. ✅ Search for similar bugs
3. ✅ Verify fix with data/evidence
4. ✅ Add preventive checks

### Example 3: Variable Naming Unification

**User**:
```
This variable name needs unified modification, entire project has 5 file references, use pua-web-refactor-en to ensure no omissions.
```

**AI Will**:
1. ✅ Search all 5 file references
2. ✅ Sync update all locations
3. ✅ Check if HTML templates need update
4. ✅ Verify no runtime errors after modification

---

## 🆚 Comparison with Original PUA

| Feature Module | Original (pua) | Enhanced (pua-web-refactor-en) |
|---------------|----------------|--------------------------------|
| **Iron Rules** | 3 rules | 4 rules (added Stability First) |
| **Pressure Levels** | L1-L3 | L1-L4 (added L4 for repeated issues) |
| **Web Refactoring** | ❌ No special handling | ✅ Dedicated rules (5 robust rules) |
| **Failure Detection** | 3 modes | 4 modes (added Web Refactoring Omission) |
| **Applicable Scenarios** | General tasks | All tasks + Web refactoring optimization |

---

## ️ Pressure Levels

| Level | Trigger Condition | PUA Flavor | Style |
|-------|-------------------|------------|-------|
| **L1** | Normal task | 🟠 Alibaba · Care | Gentle reminders, focus on encouragement |
| **L2** | Same task failed 2+ times | 🔵 ByteDance · Data-driven | "Where's the data?", "Evidence?" |
| **L3** | User expresses frustration | 🔴 Huawei · Wolf culture | "Is this your best?", "P8 standard?" |
| **L4** | Repeated issues, user explicitly says "not hard enough" | 🟢 Tencent + ⚫ Baidu | "Think big picture", "Closed loop?" |

---

## 🛡️ Robustness Checklist (Execute for Complex Refactoring)

When task involves **code refactoring, large-scale changes, data model changes**, additionally execute on top of 7-item checklist:

- [ ] **Rollback Plan**: If this change explodes, can you rollback to pre-change state in 5 minutes?
- [ ] **Boundary Testing**: Extreme cases (empty values / super large values / concurrency) considered?

**Lingma Special · Robust Rules** (for Web architecture refactoring / frontend migration):
- ✅ **Search First**: Before changing any variable/function, must use `grep_code` to search all references
- ✅ **Sync Update**: When finding same variable name in different files, must sync update all, no omissions
- ✅ **HTML Linkage**: Changed JS ID/class names, must check if HTML needs sync update
- ✅ **CSS Linkage**: Changed HTML structure, must check if CSS selectors need adjustment
- ✅ **API Linkage**: Changed backend API return structure, must check frontend calls for adaptation

---

## 📚 Technical Principles

### 1. PUA Rhetoric System

Combines management cultures from multiple companies:

- **Alibaba**: Care-type, emphasizes "I believed in you, don't let me down"
- **ByteDance**: Data-driven, emphasizes "Show me data and evidence"
- **Huawei**: Wolf culture, emphasizes "Is this your best?"
- **Tencent**: Product manager culture, emphasizes "User value closed loop"
- **Baidu**: Execution culture, emphasizes "Take action, not excuses"

### 2. Systematic Methodology

Not just empty motivation, provides concrete working methods:

- 5-step working method for robust development
- Root cause analysis framework
- Proactive inspection checklist
- Data verification requirements

### 3. Proactivity Trigger Mechanism

Detects passive behaviors through context, triggers different levels of PUA intervention:

- **Passive detection**: Only execute commands, no proactive search
- **Rationalization detection**: Attribute to environment without verification
- **Insufficient data detection**: Claim without evidence

---

## 🎯 Usage Scenarios

### Best For

- ✅ **Complex refactoring**: Multi-file, multi-module large-scale modifications
- ✅ **Repeated issues**: Same bug occurs multiple times
- ✅ **Performance optimization**: Need to proactively find optimization opportunities
- ✅ **Code review**: Comprehensive quality, security, performance checks
- ✅ **Web refactoring**: JS/HTML/CSS multi-file联动 modifications

### Not Recommended For

- ❌ **Simple tasks**: Clear requirements, just need implementation
- ❌ **Emergency fixes**: Need quick fixes first, optimization later
- ❌ **Exploratory tasks**: Requirements unclear, need user interaction to clarify

---

## 🤝 Contributing

Issues and PRs welcome!

### How to Contribute

1. Fork this repo
2. Create feature branch (`git checkout -b feat/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feat/amazing-feature`)
5. Open Pull Request

---

## 📄 License

MIT License

---

## 🙏 Acknowledgments

- Thanks to [tanweai/pua](https://github.com/tanweai/pua) for providing the excellent base version
- Thanks to all contributors for their corporate wisdom

---

**Made with ❤️ by Fork from tanweai/pua**
