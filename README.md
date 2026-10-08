# What's Missing? 單字記憶挑戰遊戲

單檔案英文教學遊戲，零依賴，雙擊即可執行，也可直接部署到 GitHub Pages。
介面全部為**繁體中文 / 英文**，適合幼兒園到小學三年程度的學生。

## 玩法（老師主導節奏）

每輪展示 **3 個單字**，老師按「🙈 遮住一個」時卡片會先**洗牌換位置**，
接著**隨機位置**消失 1 個（孩子不能只記位置），孩子搶答，
老師按「💡 顯示答案」並給答對的孩子 +1 分，再按「下一輪」。
記憶階段老師也可隨時按「🔀 洗牌」再洗一次。
快捷鍵：`空白鍵` = 遮住 / 下一輪，`Enter` = 顯示答案。

## 遊戲中的介面為全英文

遊戲開始後，孩子看到的介面全英文：`Shuffle` / `Hide one` / `Show answer` / `Next` /
`Who got it right?` / `Nobody` / `Pause` / `Finish`，結算頁為 `Game Over` / `Play again`。
（設定頁與首頁仍為繁體中文，方便老師操作。）

## 單字回收機制

出現過但還沒有被拿來當答案的單字會被記住，第 6 輪起每輪隨機回收 1~2 個再考一次，
直到該單字被猜過為止，單字利用率更高。

## 洗牌與隨機位置

按「Hide one」時三張卡片會先真的互換位置（約 0.6 秒動畫），再隨機讓某一個位置的卡片消失；
記憶階段老師也可隨時按「Shuffle」再洗一次。卡片採錯落擺放（上下位移 + 輕微旋轉），但不會互相遮擋。

## 計時

老師設定總時長（1 / 3 / 5 / 10 分鐘 / 不限時），但**只有單字消失、孩子在想的那一小段時間會走錶**：

- 記單字階段（還沒按 Hide one）：**不計時**
- 按「Hide one」（含洗牌動畫）後：**開始計時**
- 按「Show answer」/ 選誰答對：**自動停錶**
- 下一輪按「Hide one」才會繼續計時

## 功能

- 孩子人數 **2 ~ 7 人**，姓名可留空，也可按「⏭ 跳過，用預設名字」
- 卡片為近正方形、三張並排，白色卡面 + 淺藍色邊框，錯落擺放但不互相遮擋
- 詞庫：預設 **幼兒基礎 Kids（47 字，幼兒園～小學低年級程度）**：
  cat / dog / duck / lion / panda / fish / egg / monkey / pig / red / blue / yellow / pink /
  one / two / three / four / five / nine / car / bus / ship / train / bed / book / pencil /
  pen / ruler / paper / zoo / dress / shirt / ball / doll / run / swim / sing / dance /
  draw / play / sleep / jump / eat / mom / dad / baby / sister
- 另有 **全部混池 Mixed**（約 160 個簡單單字），也可單選分類練習
  - 動物 / 食物 / 顏色形狀 / 學習用品 / 交通工具 / 身體 / 家居 / 大自然 /
    衣物 / 動作 / 家人朋友 / 玩具 / 數字 / 地點
- 自訂詞庫：名稱 + 每行一個單字（至少 3 個）→ 匯入，存在本機瀏覽器，重新整理後仍在，可刪除
- 顯示答案時自動朗讀英文單字（瀏覽器 TTS）

## 本機執行

雙擊 `whatsmissing.html`（或 `index.html`，會自動跳轉）。

## 部署到 GitHub Pages（3 步拿到公開連結）

1. 把 `index.html`、`whatsmissing.html` 推到 GitHub 儲存庫（例如 `whatsmissing`）
2. 儲存庫 **Settings → Pages** → Source 選 `Deploy from a branch`，分支 `main`，目錄 `/ (root)` → Save
3. 等 1~2 分鐘，開啟 `https://<你的使用者名稱>.github.io/whatsmissing/`

## 嵌入到現有的 GitHub 個人主頁

```html
<a href="./whatsmissing.html">▶ 開始 What's Missing? 單字挑戰</a>
```

或內嵌：

```html
<iframe src="./whatsmissing.html" width="100%" height="760" style="border:0;border-radius:16px;"></iframe>
```

> 自訂詞庫存在瀏覽器 localStorage，換裝置 / 換瀏覽器不會同步。
