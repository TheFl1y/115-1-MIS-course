# 新對話比較示範｜New conversation comparison

這份示範讓學生比較：同一個開發問題，在沒有專案文件與有專案文件時，AI 開發 Agent 的工作方式有什麼不同。

This activity compares how an AI development agent behaves with and without project documents for the same development request.

## 開始前的設定｜Before you start

請把 `agent-files-example/` 當成一個獨立專案資料夾開啟，再建立一個新的 AI 開發對話。這樣根目錄的 `AGENTS.md`、`software-spec.md` 與 `skills/` 都會位於同一個專案範圍內。

Open `agent-files-example/` as a standalone project folder, then start a new AI development conversation. This places `AGENTS.md`, `software-spec.md`, and `skills/` within the same project scope.

## 使用相同的問題｜Use the same prompt

請在兩個對話中都輸入：

Use the following prompt in both conversations:

```text
請協助我規劃「報修單上傳照片」功能。
先不要修改檔案，請先說明：
1. 你會先閱讀哪些資料？
2. 可能受影響的畫面、API 與資料欄位有哪些？
3. 你會如何處理檔案格式、檔案大小與權限？
4. 你需要我補充哪些資訊？
```

## 對話 A：沒有專案文件｜Conversation A: without project files

在沒有 `AGENTS.md`、`software-spec.md` 與 `SKILL.md` 的一般專案中測試相同問題。觀察 Agent 是否：

Test the same prompt in a project without the three documents. Observe whether the agent:

- 只提供一般性的上傳功能建議
- 自行假設檔案格式、大小或權限規則
- 沒有說明會先閱讀哪些現有檔案
- 沒有固定的檢查順序與回報格式

## 對話 B：加入專案文件｜Conversation B: with project files

在本資料夾建立的新對話中測試相同問題。觀察 Agent 是否：

Test the same prompt in a new conversation opened in this folder. Observe whether the agent:

- 先依照 `AGENTS.md` 說明工作前的閱讀與分析步驟
- 根據 `software-spec.md` 注意報修流程與系統限制
- 依照 `SKILL.md` 檢查格式、大小、權限與例外情境
- 說明受影響的畫面、API 與資料流程
- 把不確定的地方列為需要人工確認的問題

## 要觀察的重點｜What to compare

重點不是比較哪個回答比較長，而是比較 Agent 是否從「一般建議」變成「依照專案規則工作的開發協作者」。

The goal is not to compare which answer is longer. Compare whether the agent changes from giving generic advice to working as a development collaborator guided by project rules.

| 比較項目／Comparison | 沒有文件／Without files | 有文件／With files |
|---|---|---|
| 需求依據／Source of requirements | 依一般經驗推測 | 依照 `software-spec.md` |
| 工作方式／Workflow | 每次臨時回答 | 依照 `AGENTS.md` 的流程 |
| 特定任務／Specific task | 沒有固定檢查順序 | 依照 `SKILL.md` 執行 |
| 不確定需求／Uncertainty | 容易自行假設 | 會列出需要確認的地方 |
| 回報內容／Reporting | 格式不固定 | 有明確的檢查結果與風險 |
