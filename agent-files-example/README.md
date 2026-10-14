# AI 開發 Agent 文件範例

這個資料夾示範如何把「校園設備報修系統」的軟體規格，整理成 AI 開發 Agent 可以依循的文件。

## 文件結構

```text
agent-files-example/
├─ README.md
├─ software-spec.md
├─ AGENTS.md
└─ skills/
   └─ repair-review/
      └─ SKILL.md
```

## 三個核心文件

- `software-spec.md`：說明系統目標、功能、限制與完成條件。
- `AGENTS.md`：說明 Agent 在這個專案中應如何工作。
- `skills/repair-review/SKILL.md`：說明檢查報修功能時可以重複使用的方法。

這些文件不綁定特定 AI 工具；實際使用時，請依所選工具支援的文件格式與資料夾規範調整。
