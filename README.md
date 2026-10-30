# 菲米諾吸音板｜GitHub Pages 網站重建說明

這是「保留 GitHub Repository、重新上傳網站檔案」的**可直接部署版本**。

- 品牌：菲米諾吸音板
- 標語：以靜成就非凡
- GitHub 專案：https://github.com/felisa-code/felmenon
- 正式網址：https://felisa-code.github.io/felmenon/
- 頁面入口：`index.html`（大小約 6.1 MB）
- 部署方式：GitHub Pages → Deploy from a branch → `main` → `/(root)`

## 這一層的檔案可直接上傳

```text
index.html                 網站首頁；已內建 30 頁型錄的 JPG 資料
catalog.pdf                30 頁完整版型錄的網頁壓縮檔，約 16 MB
brand-song.mp3             菲米諾〈以靜成就非凡〉形象歌曲（不自動播放）
logo-horizontal.jpg        頁首橫式中文品牌 Logo
logo-vertical.jpg          形象區直式中文 Logo
case1.jpg ～ case7.jpg      七張室內吸音板案例照片
.nojekyll                  讓 GitHub Pages 直接處理靜態檔案
README.md                  本說明
```

> 注意：**不需要 `pages` 資料夾**。30 頁圖已內嵌於 `index.html`，避免此前 `pages/page-01.jpg` 失聯造成的破圖。

## 網頁版操作（保留現有 Repository）

1. **先備份**：開啟 https://github.com/felisa-code/felmenon → `Code` → `Download ZIP`，保存舊站。
2. 解壓本資料包；只使用此 `01_網站上傳檔案` 資料夾裡的檔案，**不要直接上傳 ZIP 檔**。
3. 專案原本已有 `index.html`，不要讓 Windows 將新版自動更名為 `index (2).html`。推薦先在 GitHub 上備份舊版（ZIP 已備份），再用 GitHub 網頁上傳同名檔替換；若 GitHub 阻止覆蓋，才在 GitHub 檔案頁刪除舊 `index.html`、`Commit changes`，隨即 `Add file` → `Upload files` 上傳本版 `index.html` 並 `Commit changes`。刪除到新版部署成功之前可能短暫 404。
4. 如果 GitHub 缺少 Logo、案例圖、`brand-song.mp3` 或 `catalog.pdf`，到 `Add file` → `Upload files` 上傳**缺少的檔案**。上傳前務必確認檔名與 `index.html` 裡的檔案路徑完全一致。
5. 依序開啟 `Settings` → `Pages`，確認 `main` + `/(root)`；若原本已設定正確，不必更動。
6. 開啟 `Actions` 確認 Pages 部署顯示綠勾，再用無痕視窗開啟 https://felisa-code.github.io/felmenon/ 。
7. 測試：Logo、歌曲播放、型錄 1→2→30 頁、上一頁/下一頁、手機左右滑動、放大縮小、PDF 開啟下載、7 張案例照片、官方社群連結。
8. **成功後**才清除不再需要的 `index (2).html`、`flipbook-test...` 等測試檔；本資料包的驗證版建議保存在電腦，不必上傳。

GitHub 瀏覽器介面單個檔案一般有約 25 MiB 上傳限制；本站的 16 MB `catalog.pdf` 可以上傳，但原始 42 MB PDF 請不要直接透過網頁版上傳 GitHub，保留在完整備份即可。

## 網站功能

- 響應式單頁品牌網站：首頁、形象歌曲、電子型錄、案例照片、官方連結。
- 30 頁型錄使用內嵌 JPG 和 CSS/JavaScript 擬真翻頁效果，不依賴 `pages/page-xx.jpg`。
- 支援上一頁／下一頁、手機觸控翻頁、鍵盤左右方向鍵、放大／縮小與頁碼；並可開啟／下載 PDF。
- 歌曲由訪客自行操作，無自動播放。
- 案例照片支援點選放大。

## 品牌官方連結（可依最新官方資料再核對）

- 官方網站：https://www.acasa.com.tw/
- LINE：https://page.line.me/acasa
- Facebook：https://www.facebook.com/Felmenon.tw/
- Instagram：https://www.instagram.com/felmenon.tw/
- YouTube：https://www.youtube.com/@FelmenonTW

## 重要備註

- 本資料夾的 `index.html` 是從過去**已確認能正常翻閱的 v3** 衍生的正式首頁版；保留原本測試版的 30 頁圖片資料，但去除了測試訊息及 `noindex` 標籤。
- `catalog.pdf` 是便於 GitHub 網頁上傳的壓縮版本，**不是**原始 42 MB PDF。原始檔和 30 張型錄頁面 JPG 在完整備份包內。
- 目前已進行**本地檔案結構、30 張型錄圖、JavaScript 語法與 PDF 頁數檢查**；受測試環境限制，未能完成實際瀏覽器互動驗收，也尚未替使用者更新線上的 GitHub Repository，線上版本應以使用者部署後為準。
- 網站公開後，所有圖片、音樂與型錄可被訪客讀取／下載，使用前需確認適合公開。
