# 霍華德餐館 點餐網站

給朋友點餐用的小網站，放在 GitHub Pages 上，不用伺服器。

- `index.html`：網站本體
- `menu.json`：菜單內容（餐館名稱、招呼語、收信 Email、每道菜）
- `images/`：編輯時上傳的菜色照片

## 三個功能

1. **網站**：朋友打開網址就能選菜。
2. **點餐寄信**：朋友按「送出點餐（寄給主廚）」，點餐內容直接寄到 `menu.json` 裡的 Email，經由 [FormSubmit](https://formsubmit.co)。也可以改用 LINE 傳，或複製內容。
3. **連點 10 下 Logo 編輯**：店主在自己的裝置上連點左上角的廚師 Logo 10 下，就能新增、修改、刪除菜色、換照片、改設定。按「儲存」後，網站會把變更寫回這個 repo，約 1 分鐘後朋友就會看到。

## 第一次設定

### 1. 開啟 GitHub Pages

GitHub 免費方案只有公開 repo 能用 Pages。

1. repo 的 **Settings → General → Danger Zone → Change visibility**，改成 **Public**。
2. **Settings → Pages**：Source 選 **Deploy from a branch**，Branch 選放網站的分支、資料夾選 **/ (root)**，按 Save。
3. 約 1 分鐘後，網址會出現在同一頁，格式是 `https://<帳號>.github.io/<repo 名稱>/`。

### 2. 啟用點餐寄信（只要做一次）

1. 打開網站，自己點一次餐，按「送出點餐（寄給主廚）」。
2. 到收信信箱找 FormSubmit 寄來的確認信，按 **Activate Form**。
3. 之後朋友的點餐就會直接寄到你的信箱。

### 3. 建立編輯用的 GitHub 金鑰

1. 打開 <https://github.com/settings/personal-access-tokens/new>。
2. **Repository access** 選 **Only select repositories**，只選這個 repo。
3. **Permissions → Repository permissions → Contents** 設成 **Read and write**。
4. 按 **Generate token**，複製金鑰。
5. 在網站上連點 Logo 10 下，把金鑰貼進去登入。

金鑰只會存在你登入的那台裝置的瀏覽器裡，不會放進網站或 repo。朋友沒有金鑰，連點也不能編輯。要清掉金鑰，進編輯模式後按「設定 → 登出這台裝置」。

## 注意

- 網站是公開的，`menu.json` 裡的 Email 任何人都看得到。
- 儲存後 GitHub Pages 需要約 1 分鐘重新發布；手機若還看到舊菜單，重新整理即可。

---

# 球衣名字產生器

網址：`https://<帳號>.github.io/<repo 名稱>/jersey/`

輸入名單（每行「名字, 號碼」），每個人產生一個 STL，對齊 60 mm 空白球衣，直接匯入 Bambu Studio。

- 名字和號碼共用同一個字體，可以上傳自己的 `.ttf` / `.otf`（例如 Jersey M54），這台裝置會記住。
- 「下載這件」會直接下載一個 `.stl`；「下載全部 STL」會一個一個下載，瀏覽器若問「允許下載多個檔案」，請按允許。
