# 設定說明

## 課前完成

GitHub 帳號已登入並驗證信箱。Make、LINE、OpenRouter 依原教材建立完成，傳送虛構文字時已有正常回覆。正式憑證僅留在服務端連線設定，不放入這個資料夾。

## Pages

1. 在自己的 GitHub 建立公開練習 repo，例如 `linebot-workshop`。
2. 根目錄放 README.md、setup.md、scenario-outline.md、test-cases.md、.gitignore。
3. `index.html` 放在 `docs` 內，不能多包一層 `public-project`。
4. Settings / Pages / Build and deployment。
5. Source 選 Deploy from a branch。
6. Branch 選 main，資料夾選 /docs，按 Save。
7. 在 Actions 查看發布工作，回 Pages 取得網址，實際開啟。

免費帳號的這條練習路線使用公開 repo，所有檔案都會公開。不要將已有業務資料的私有 repo 改成公開。

## LINE 連結

從自己測試用官方帳號後台取得公開「加入好友」網址。它與 Make Webhook、LINE Developers Console 網址不同。只將公開加入好友網址放進網頁。

## Make

保留原來 LINE Developers 中的 Make Webhook，勿替換成 Pages 網址。保存 Scenario 並開啟立即執行。Run once 只用於單次測試。確認連線及模型仍可用，不保證免費模型或額度。

正式服務另需確認 LINE 簽章驗證、重送去重、例外處理與資料保存規則。本課範例網頁不補足這些後端安全功能。
