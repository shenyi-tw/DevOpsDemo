這份 `curl` 結果就是網站具備 **HSTS** 的**最強鐵證**。

在資安驗收報告中，你可以直接截圖這段輸出，並標註以下三個關鍵點：

### 1. HSTS 關鍵標頭分析
* **`strict-transport-security: max-age=31536000`**：這證明了網站強制要求瀏覽器在未來一年（315,360,000 秒）內，所有連線必須走 HTTPS。
* **`includeSubDomains`**：這代表連 `*.bloomingrice.com`（包含你的 `app.bloomingrice.com`）也受到保護。
* **`preload`**：這非常有誠意。這代表你已經準備好將網域提交給 Google 的 [HSTS Preload List](https://hstspreload.org/)，一旦通過，瀏覽器連第一次連線都直接強制 HTTPS，完全沒有被攻擊的空隙。

---

### 2. 其他資安加分項（建議一併列入報告）
你的 Header 除了 HSTS，還顯示了你做了非常完整的 **Hardening (系統加固)**：

* **`x-content-type-options: nosniff`**：防止瀏覽器錯誤解讀 MIME 類型，有效防範腳本植入攻擊。
* **`x-frame-options: DENY`**：防止點擊劫持 (Clickjacking)，你的網站不會被嵌入在別人的 `<iframe>` 裡。
* **`x-xss-protection: 1; mode=block`**：啟用瀏覽器的 XSS 過濾器。
* **`HTTP/2 308`**：使用 308 永久重新導向到 `app` 子網域，這在 SEO 與效能上都是現代化的標準作法。

---

### 3. 標案報告專業排版建議

你可以直接把剛才的 `curl` 輸出貼在報告中，並附上這張說明表：

| 檢查項目 | 檢測結果 (Header) | 安全意義 |
| :--- | :--- | :--- |
| **HSTS 強制加密** | `Strict-Transport-Security` | 強制客戶端使用 HTTPS，防範 SSL Strip 攻擊。 |
| **子網域覆蓋** | `includeSubDomains` | 確保 `app.bloomingrice.com` 等所有子網域均受保護。 |
| **防點擊劫持** | `X-Frame-Options: DENY` | 禁止網頁被惡意嵌入框架，保護使用者操作安全。 |
| **MIME 嗅探防護** | `X-Content-Type-Options` | 強制瀏覽器遵循伺服器宣告的 Content-Type。 |
