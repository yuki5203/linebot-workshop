# 課堂 LINE 客服示範

這是 GitHub 常用功能與安全發布的練習專案，包含使用文件與靜態服務介紹頁。

## 服務分工

- GitHub 保存這份專案的文件與版本。
- GitHub Pages 發布 `docs/index.html`。
- LINE 訊息由原本的 Make Scenario 處理，Make 呼叫 OpenRouter 並回覆 LINE。
- Google Sheets 與 Gmail 草稿為原教材的選用功能，仍由 Make 執行。

上傳這些檔案不會建立或啟動 Make Scenario。本專案沒有後端、API key、Webhook，也沒有可直接匯入的 Make Blueprint。

## 使用方式

1. 閱讀 [設定說明](setup.md)，確認自己已有可回覆的測試機器人。
2. 修改 `docs/index.html` 的服務名稱與用途。
3. 依實作手冊將停用的入口換成自己測試帳號的公開加入 LINE 連結。
4. 以 `main` 分支、`/docs` 為來源啟用 Pages。
5. 依 [測試案例](test-cases.md) 實際驗收。

## 資料保護

不要加入憑證、完整 Make Webhook、客戶訊息、LINE userId、私人信箱、試算表資料或原始執行紀錄。金鑰保留在 Make 連線管理中。本課只使用虛構訊息。

`.gitignore` 不是機敏資料掃描器，無法清理既有歷史，也不能作為網頁上傳的保護。每次上傳及提交前都要逐檔檢查。

## 專案檔案

- `docs/index.html`：公開介紹頁，無外部 API 呼叫。
- `setup.md`：設定步驟。
- `scenario-outline.md`：依原 MD 整理的 Make 流程說明。
- `test-cases.md`：虛構測試案例。
- `.gitignore`：本機 Git 的輔助排除規則。

## 授權

這份範例供本課教學使用。若要以開源專案對外散布，請先確認所有素材的權利並選擇適當授權。本練習不自動替公司或第三方素材授權。
