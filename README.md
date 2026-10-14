# 校園設備報修系統｜Campus Equipment Repair System

這是一個為資訊管理課程設計的校園設備報修系統範例。使用者可以透過網頁填寫報修內容，管理人員可以查看案件並更新處理狀態。這個專案也示範如何把軟體規格整理成 AI 開發 Agent 可以依循的工作文件。

This is a small campus equipment repair system created for an Information Management course. Users can submit repair requests through a web form, while staff members can review requests and update their status. The repository also demonstrates how software specifications can be organized into documents that an AI development agent can follow.

## 這個專案適合誰？｜Who is this repository for?

這個專案適合以下讀者：

- 想了解前端表單如何把資料送到後端的初學者
- 想觀察 Flask API 與網頁介面如何互相配合的學生
- 想練習閱讀軟體規格、開發規則與工作流程的人
- 想了解如何讓 AI 開發 Agent 依照專案規則工作的讀者

This repository is intended for:

- Beginners who want to understand how a web form sends data to a backend
- Students learning how Flask APIs work with a browser interface
- Anyone practicing how to read software specifications and development workflows
- Readers who want to learn how to give an AI development agent clear project rules

## 系統可以做什麼？｜What can the system do?

目前的範例包含：

- 使用者填寫設備、地點、問題描述與聯絡方式
- 後端接收報修資料並產生案件編號
- 管理人員查看所有報修案件
- 管理人員更新案件處理狀態
- 前端與後端透過 API 傳遞資料

The current example includes:

- A form for equipment, location, problem description, and contact information
- A backend endpoint that receives a request and generates a ticket number
- An administrative page for viewing submitted requests
- Status updates for repair requests
- Communication between the browser and backend through APIs

## 如何在自己的電腦上執行？｜How to run the project

### 系統需求｜Requirements

- Windows 10 or Windows 11
- Python 3.13 or a compatible Python version
- A modern browser such as Microsoft Edge or Google Chrome

### 第一次執行｜First-time setup

在此 Repository 的資料夾中開啟 PowerShell，依序執行：

Open PowerShell in the repository folder and run:

```powershell
python -m venv .venv
.\\.venv\\Scripts\\python.exe -m pip install -r requirements.txt
.\\.venv\\Scripts\\python.exe app.py
```

看到以下訊息後，在瀏覽器開啟 <http://127.0.0.1:5000>：

When you see the following message, open <http://127.0.0.1:5000> in your browser:

```text
Running on http://127.0.0.1:5000
```

管理後台位於 <http://127.0.0.1:5000/admin>。按下 `Ctrl + C` 可以停止伺服器。

The administration page is available at <http://127.0.0.1:5000/admin>. Press `Ctrl + C` to stop the server.

### 之後再次執行｜Run it again later

```powershell
.\\.venv\\Scripts\\python.exe app.py
```

## 建議的閱讀順序｜Suggested reading order

如果你是第一次閱讀這個專案，可以依照以下順序：

If this is your first time exploring the repository, follow this order:

1. 先閱讀本頁，了解系統用途與啟動方式。／Read this page first to understand the purpose and setup.
2. 閱讀 `templates/index.html`，找出使用者填寫報修資料的表單。／Read `templates/index.html` to find the request form.
3. 閱讀 `static/app.js`，觀察前端如何呼叫 `fetch("/api/tickets")`。／Read `static/app.js` to see how the browser calls `fetch("/api/tickets")`.
4. 閱讀 `app.py`，了解後端如何接收、驗證並回傳資料。／Read `app.py` to see how the backend receives, validates, and returns data.
5. 閱讀 `templates/admin.html` 與 `static/admin.js`，觀察管理人員如何更新狀態。／Read `templates/admin.html` and `static/admin.js` to see how staff update ticket status.
6. 閱讀 `agent-files-example/`，了解如何把軟體規格整理成 Agent 工作文件。／Read `agent-files-example/` to learn how a specification becomes agent-facing documentation.

## AI 開發 Agent 文件範例｜AI development agent example

`agent-files-example/` 是一個獨立的教學範例，內容包含：

`agent-files-example/` is a separate teaching example containing:

- [`software-spec.md`](agent-files-example/software-spec.md)：說明系統要解決什麼問題、有哪些功能與限制。／Describes the problem, features, and constraints.
- [`AGENTS.md`](agent-files-example/AGENTS.md)：說明 Agent 在專案中應該如何工作。／Describes how the agent should work in the project.
- [`SKILL.md`](agent-files-example/skills/repair-review/SKILL.md)：整理檢查報修功能時可以重複使用的步驟。／Describes a reusable process for reviewing repair features.

這些文件不是某一個特定 AI 工具專用的格式。不同工具可能有不同的資料夾或檔名規範，但核心概念相同：把需求、限制、工作步驟與回報方式說清楚。

These files are not limited to one specific AI tool. Different tools may use different folder or naming conventions, but the central idea is the same: clearly describe the requirements, constraints, workflow, and reporting format.

## 教學上的限制｜Teaching limitations

這是一個為課堂示範而簡化的系統，不是可直接部署到正式校園環境的產品。目前案件資料只保存在 Python 程式的記憶體中，停止或重新啟動程式後，資料會被清除。正式系統還需要資料庫、登入驗證、權限管理、檔案儲存、操作紀錄與安全性檢查。

This system is intentionally simplified for classroom demonstration and is not ready for production deployment. Ticket data is stored only in Python memory, so it is cleared when the application stops or restarts. A production system would also need a database, authentication, authorization, file storage, audit logs, and additional security controls.

## 課程作業參考｜Course assignment reference

學生可以參考 `agent-files-example/` 的結構，將自己小組的軟體規格整理成一組可分享的 Agent 文件。GitHub 用來放置完整檔案，課程平台則提交 Repository 連結。

Students may use `agent-files-example/` as a structural reference and turn their own group’s software specification into a shareable set of agent documents. GitHub stores the complete files, while the course platform is used to submit the repository link.
