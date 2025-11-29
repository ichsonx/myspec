# OpenSpec 自定义规范模板

本模板用于实践 **"需求 → 场景 → 用户故事 → 任务"** 的轻量级规范驱动开发。

## 🚀 快速开始

1. **创建需求目录**
   ```bash
   mkdir -p openspec/changes/REQ-2025-002_export-to-csv
   ```

2. **复制模板**
   将 `spec.md` / `tasks.md` 模板放入该目录，按需修改内容。

3. **启动 AI 协作**
   对 AI 说：
   > "请基于 openspec/changes/REQ-2025-001-filename_rebuild/ 下的 spec.md 和 tasks.md，按 agents.md 规范启动开发协作。"

## 📂 目录结构说明
```
openspec/
└── changes/
    └── REQ-{YEAR}-{SEQ}_{slug}/
        ├── spec.md     # 完整需求文档（PRD）
        └── tasks.md    # 可执行任务清单
        └── agents.md   # AI协作协议
```

## 🔍 关键设计原则
- **需求 ID 全局唯一** → 支持跨文档追踪  
- **场景 = 验收单元** → 每个场景对应一组可验证行为  
- **用户故事 = 技术视角拆解** → 无模糊"作为...我希望..."，直接归属场景  
- **任务 = 最小可交付单元** → `[ ]` → `[x]` 状态自包含
- **内容可选** → 除需求ID、背景、目的目标外，其他内容允许为空
- **AI真实性** → AI不得虚构、臆想或伪造数据和实现细节