# 阪木老大實驗室 v1.4.2

《寶可夢 心金／魂銀》Gen IV 存檔修改器。

## v1.4.2 — 存檔完整性修正
- Block 選擇順序：先 CRC/footer 完整性，再依 Gen IV 的 major/minor counter 判定新舊。
- General 與 Storage 各自獨立選擇有效的最新 Block，不再強迫 counter 配對。
- 匯出時若另一份主／備份 Block 已損壞，會用目前有效 Block 的資料修復它，而不是把損壞資料重新標成有效。
- 修復時保留該備份原本的 counter（若可用），再重新計算 CRC。
- 下載前強制驗證兩份 General + 兩份 Storage，共 4 個主要 Block 全部 CRC/footer 有效。
- 即使沒有修改寶可夢，只要偵測到主／備份 Block 損壞，也會開放匯出「修復檔」。
- 修改後回讀驗證以「匯出檔真正會被選中的 active Block」為準，避免只驗證原始偏移。
- 保留 v1.4.1 的圖片、暱稱、等級／性別顯示、EV／IV／個性修改功能。

網站：https://kane6353.github.io/HGSS-EV-Editor/
