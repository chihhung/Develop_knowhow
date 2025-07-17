# AI 程式設計助理指引 - Develop_knowhow

## 專案概述
這是一個全面性的**中文軟體開發知識庫**（`專案開發人員參考`），設計為專案開發人員提供結構化的參考指南。本專案採用階層式文件組織模式，以主要的 README.md 作為總索引。

## 架構與結構

### 核心文件組織模式
- **主要 README.md**：總索引，包含編號章節（0-7）和對應的目錄連結
- **docs/{分類}/README.md**：分類首頁，提供子主題導覽
- **巢狀結構**：大部分內容位於 `docs/Programming_Languages_​​and_Development_Environments/`（注意路徑中的 Unicode 字元）

### 主要分類（如主 README 中定義）
1. 資訊人員的角色與職責
2. 程式語言與開發環境 - **主要內容區域**
3. 前後端平台
4. 程式設計心法
5. 系統與架構設計
6. DevOp
7. 專案管理

## 內容慣例

### 檔案命名與路徑
- 目錄名稱使用**中文命名**來表示中文概念
- README.md 檔案為主要內容容器
- 導覽使用 `[< backto專體開發從業人員參考](../../README.md)` 模式作為麵包屑導覽
- 某些路徑包含 Unicode 字元（例如：`Programming_Languages_​​and_Development_Environments`）

### 文件撰寫風格
- **雙語混合方式**：中文標題配合英文技術術語
- 技術內容經常包含實用範例（參見 `git/README.md` 的多帳號 SSH 設定）
- 程式碼區塊使用三個反引號並指定語言
- 導覽連結使用相對路徑並適當轉義

### 技術涵蓋範圍
本知識庫涵蓋的開發工具和語言包括：
- **程式語言**：Java、Python、JavaScript、TypeScript、SQL、HTML/CSS
- **開發工具**：Git、GitHub、GitLab、VS Code、Eclipse、IntelliJ、Maven、Postman、JMeter
- **開發平台**：Vue3、Angular、Spring Boot
- **方法論**：Clean Code、設計模式、Clean Architecture、TOGAF

## 開發工作流程

### 內容建立模式
1. 新增主題時更新主 README.md 的條列項目
2. 在目錄區段新增對應的導覽連結
3. 在適當的 docs 分類下建立目錄結構
4. 為新 README 檔案新增麵包屑導覽

### 檔案管理
- 大部分內容檔案目前為空白佔位符（待擴充）
- 目前僅 `git/README.md` 包含實質的技術內容
- 維持中英文混合方式以提升可用性

## 特殊考量

### 路徑處理
- 注意 `Programming_Languages_​​and_Development_Environments` 路徑中的 Unicode 字元
- 程式化參照檔案時使用絕對路徑
- 文件導覽使用相對連結

### 內容擴充
新增內容時：
- 遵循既有的中文命名慣例用於使用者導向的分類
- 特定技術使用英文術語
- 包含實用範例，如 Git 多帳號設定
- 維持麵包屑導覽模式
- 同時更新主 README 的條列項目和目錄連結

本知識庫作為**中文開發者的活知識庫**，強調實用指導勝過理論概念。
