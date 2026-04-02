---
schema: agentcompanies/v1
---

# Adversarial Governance Company

A generic, product-agnostic AI agent company framework with built-in adversarial governance for [Paperclip](https://github.com/paperclipai/paperclip).

**32 agents. 10 governance rules. Zero product assumptions.**

## What Is This?

A ready-to-import company package that gives you a complete organizational structure with checks and balances. Import it into any Paperclip instance, then customize for your specific product and tech stack.

## Org Chart

```
CEO (執行長)
├── CTO (技術長)
│   ├── 品質工程經理 ────────── [blocks releases]
│   │   ├── 程式碼審查員 ────── [challenges ALL code]
│   │   └── 測試工程師
│   ├── 設計主管
│   │   ├── 設計構思師
│   │   └── 設計轉碼師
│   ├── 基礎設施經理
│   ├── 發佈經理 ──────────── [triple sign-off required]
│   │   ├── 部署工程師
│   │   └── 金絲雀部署員 ──── [blocks deployment]
│   └── 軟體工程師
├── CSO (安全長) ──────────── [independent, vetoes CTO]
│   └── 安全維運員 ────────── [intercepts ALL agents]
├── CFO (財務長) ──────────── [financial veto]
├── PM (產品規劃師) ─────── [independent, vetoes CTO on scope]
├── CMO (行銷長)
│   ├── 內容策略師
│   │   ├── SEO 專員
│   │   └── 影音內容製作
│   ├── 社群經理
│   ├── 成長專員
│   │   └── 廣告投放專員
│   ├── 品牌審查員 ────────── [reviews ALL external content]
│   ├── KOL 合作專員
│   ├── 電商營運專員
│   └── 客服主管
│       └── 客服專員
├── 法務合規官
├── 業務開發經理
└── 計畫審查員 ────────────── [challenges CEO + CTO plans]
```

## 10 Governance Rules

### Technical (5)
1. **CSO vetoes CTO** on security — only CEO can override
2. **PM vetoes CTO** on product scope — only CEO can override
3. **Quality Manager blocks releases** — CTO cannot override
4. **Canary blocks deployment** — abnormal metrics = stop
5. **Three-party consent** — major decisions need CTO + CSO + PM

### Business (5)
6. **Brand Reviewer reviews all external content** before publishing
7. **CSO reviews growth strategies** for compliance
8. **PM reviews marketing content** for product accuracy
9. **CFO reviews BD commitments** for financial viability
10. **CSO reviews BD partnerships** for security/compliance

## Quick Start

```bash
# Import into your Paperclip instance
paperclipai company import https://github.com/YOUR_USERNAME/adversarial-governance

# Or from a local directory
paperclipai company import ./adversarial-governance
```

After import:
1. Configure adapters for each agent (Claude Code, Codex, etc.)
2. Add your product-specific context to CEO, CTO, and PM instructions
3. Add domain-specific skills
4. Start creating tasks

## Customization Guide

### Adding Engineers
The default `engineer` is a generalist. Clone and specialize:
- Frontend Engineer, Backend Engineer, Data Engineer, etc.
- Set `reportsTo: cto` and add role-specific instructions

### Adding Governance Rules
When adding new roles that can trigger external actions:
- Require at least dual sign-off
- Define veto scope for new C-suite roles
- Document adversarial relationships bidirectionally

### Scaling Customer Service
The `cs-lead` already has a `support-agent` for first-line support. Add more Support Agents as volume grows.

## Design Principles

- **No heartbeat instructions** — Paperclip skill handles all coordination
- **No product context** — add after import
- **No adapter specified** — configure after import
- **Assignment-only** — agents wake when assigned tasks
- **Traditional Chinese instructions** — English slugs for compatibility

## License

MIT
