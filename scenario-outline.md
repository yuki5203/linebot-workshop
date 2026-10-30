# Make 流程說明

這是文件，不是 Blueprint，不能匯入 Make。原始來源為使用者提供的 Make AI LINE 客服教學 MD。

1. **Custom webhook**：接收 LINE 傳來的事件。網址僅保存在 LINE 後台與 Make。
2. **事件檢查**：先處理空事件與非文字事件。正式使用前確認簽章驗證及事件重送去重。
3. **OpenRouter / Create a chat completion**：將文字事件的 `message.text` 映射到訊息內容，使用個人的安全連線及可用模型。
4. **LINE / Send a Reply Message**：使用當次事件的 `replyToken`，將模型回應映射為文字。
5. **Google Sheets / Add a row（選用）**：只在測試用表格記錄虛構測試資訊。
6. **Gmail / Create a draft email（選用）**：只建立草稿。不得擅自寄出或使用真實客戶資料。
7. 保存 Scenario 並啟用立即執行，回 LINE 驗收。

## Blueprint 備份

原始匯出檔存到 repo 以外的本機私有資料夾。匯出設定仍可能包含手寫文字、網址、識別碼、收件人或敏感的固定值。未逐項審查的 JSON 不上傳。

需要還原時，先建立新的測試 Scenario，匯入私有備份，再設定自己的連線與 Webhook。勿覆寫既有流程。重新連線後的版本不可反向公開。

## 原教材需注意的地方

原 MD 的「不要按 Verify」不能作為通用規則。LINE 驗證請求可能包含空 `events`，流程應能正確回應且不呼叫模型。收到事件也應確認來源簽章，不能只靠 Webhook 網址難以猜測。

參考：
- https://help.make.com/blueprints?lang=en
- https://developers.line.biz/en/docs/messaging-api/receiving-messages/
- https://developers.line.biz/en/docs/messaging-api/verify-webhook-signature/
