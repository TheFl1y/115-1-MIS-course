# AI 開發 Agent 文件範例｜AI Development Agent Files Example

這個資料夾示範如何把「校園設備報修系統」的軟體規格，整理成一組 AI 開發 Agent 可以閱讀、理解並依循的文件。

This folder demonstrates how to turn the software specification of a campus equipment repair system into a set of documents that an AI development agent can read, understand, and follow.

## 為什麼需要這些文件？｜Why do we need these files?

如果只對 AI 說「請幫我修改報修功能」，它可能只根據當下的問題產生答案，卻不一定知道這個專案的限制、資料流程與團隊習慣。

If we only tell an AI, “Please modify the repair feature,” it may respond to the immediate request without understanding the project’s constraints, data flow, or team conventions.

這三個文件把不同類型的資訊分開保存：

These three documents keep different kinds of information separate:

- 規格書說明系統要完成什麼。／The specification explains what the system should accomplish.
- 工作規則說明 Agent 應該如何修改專案。／The project rules explain how the agent should make changes.
- Skill 說明某一類任務可以按照什麼步驟處理。／The Skill explains how to handle a particular type of task step by step.

## 文件結構｜File structure

```text
agent-files-example/
├─ README.md
├─ software-spec.md
├─ AGENTS.md
└─ skills/
   └─ repair-review/
      └─ SKILL.md
```

## 三個核心文件｜The three core files

### `software-spec.md`

說明系統的目標、使用者、功能、限制與完成條件。它回答的是：「這個系統要解決什麼問題？做到什麼程度才算完成？」

This file describes the system goal, users, features, constraints, and completion criteria. It answers: “What problem does the system solve, and what counts as complete?”

### `AGENTS.md`

說明 Agent 在這個專案中扮演的角色、修改前要做什麼、修改時要遵守哪些規則，以及完成後要回報哪些資訊。

This file describes the agent’s role, what it must do before editing, which rules it must follow, and what it must report after the work is complete.

### `skills/repair-review/SKILL.md`

說明在檢查報修功能時可以重複使用的流程，包括檢查順序、需要注意的例外，以及最後的輸出格式。

This file describes a reusable process for reviewing repair features, including the review order, important edge cases, and the expected output format.

## 如何使用這個範例？｜How to use this example

1. 先閱讀 `software-spec.md`，了解系統需求。／Read `software-spec.md` to understand the requirements.
2. 再閱讀 `AGENTS.md`，了解專案工作規則。／Read `AGENTS.md` to understand the project rules.
3. 當任務涉及報修功能時，參考 `SKILL.md` 的檢查流程。／When the task involves a repair feature, follow the review process in `SKILL.md`.
4. 將這個結構改寫成自己小組系統的版本。／Adapt this structure to your own group’s system.

## 如何比較有沒有這些文件的差異？｜How to compare the difference

請把本資料夾 `agent-files-example/` 當成一個獨立專案開啟，再建立新的 AI 開發對話。這樣 `AGENTS.md` 會成為專案根目錄的工作規則，`software-spec.md` 是系統需求依據，而 `skills/repair-review/SKILL.md` 則提供報修功能的檢查流程。

Open `agent-files-example/` as a standalone project, then start a new AI development conversation. In this setup, `AGENTS.md` provides project-level rules, `software-spec.md` provides the system requirements, and `skills/repair-review/SKILL.md` provides a review workflow for repair features.

請使用相同的功能問題，先在沒有這些文件的專案中詢問，再在本資料夾的新對話中詢問。完整的比較提示與觀察重點請參考 [`DEMO.md`](DEMO.md)。

Use the same feature request first in a project without these files and then in a new conversation opened in this folder. See [`DEMO.md`](DEMO.md) for the comparison prompt and observation checklist.

這些文件不綁定特定 AI 工具。不同工具可能要求不同的檔名或資料夾位置，使用前請依照所選工具的文件格式調整。

These files are not tied to a single AI tool. Different tools may require different names or folder locations, so adapt the structure to the conventions of the tool you choose.
