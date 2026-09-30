# ⚽ 智能量化足球預測系統 ver 1.0

工具: https://thevker.github.io/FootBall-AI/

> 一套結合**機率模型、市場定價（賠率）與極致風控**的自動化足球分析工具。用數學邏輯取代人為情緒，適用於足球賽前數據分析與策略驗證。

![Version](https://img.shields.io/badge/version-1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML](https://img.shields.io/badge/HTML-5-orange)
![CSS](https://img.shields.io/badge/CSS-3-blue)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)

---

## 📸 預覽

> 五合一系統：**條款同意頁 + 智能預測計算器 + 猜賽果挑戰 + 排行榜 + 即時模擬測試**

- 🌙 直接深淺色主題切換
- 🌐 繁中 / 簡中 / 英文
- 📊 實時讀取 Google Sheets 真實賽事數據
- 🎮 遊戲化猜賽果 + Tier 等級系統 + 連勝特效
- 🏆 Top 10 / Top 100 排行榜 + 玩家上傳成績
- 🧪 即時模擬測試（終端機風格，逐場顯示）
- 📱 響應式設計（手機 / 平板 / 電腦）
- 🔒 賽果數據 ±5% 隨機微調，防止玩家搜尋反查作弊

---

## ✨ 功能特色

### 🧮 智能預測計算器
- 輸入 **6 個數據**（主/和/客勝率 + 主/和/客賠）
- **14 層公式** 輸出建議：**買主 / 買和 / 買客 / 不出手**
- 自動計算 **期望值 EV-1**
- 顯示該層策略邏輯說明
- 勝率總和必須 ≤ 100%

### 🎮 猜賽果挑戰
- **從 Google Sheets 真實數據隨機抽樣**
- **每場勝率、賠率 ±5% 隨機微調**（防止玩家搜尋原始數據作弊），賽果與比分保持真實
- 顯示真實比分與賽果
- 每注固定 **$100**
- **⏭️ 跳過功能**：預設 2 次，每玩 10 場 +1 次
- **🔥 連勝特效**：連續命中 3 場以上彈出火焰連勝提示（固定大小，不遮擋按鈕）
- **Tier 等級系統**（5 場後顯示）：
  - 綜合分數 = **命中率 × 50% + ROI × 100%**（上限 100 分）
  - **分數範圍 0.00 ~ 100.00**（ROI 負值視為 0，ROI 上限封頂 100）
  - 🟣 **EX**：紫色幻彩漸變色 + 紫色文字 + 發光呼吸特效
  - 🟡 **S / S+ / S-**：金色漸變
  - 🔵 **A / A+ / A-**：冰藍漸變
  - 🟢 **B / B+ / B-**：淺綠漸變
  - 🔴 **C / C+ / C-**：紅色漸變
  - ⚪ **D / D+ / D-**：灰色漸變
  - 🟤 **E / E+ / E-**：啡色漸變
  - **同級同**，換級有漸變過渡效果
  - **⬆️ 升級** 顯示綠色箭頭 + 邊框閃光
  - **⬇️ 降級** 顯示紅色箭頭 + 邊框閃光
- 賽事描述：💥 史詩級大爆冷 / 💰 高賠和局 / ✅ 正常賽果 …

### 🧪 即時模擬測試
- 使用**當前公式參數**對**資料庫全部真實數據**回測
- **逐場即時計算**（終端機風格，綠色＝命中 / 紅色＝落敗 / 灰色＝跳過）
- 顯示：場次編號 / 勝率 / 賠率 / 觸發層 / 出手選擇 / 實際賽果 / 盈虧 / 累計盈虧
- 完成後顯示完整報告：
  - 總樣本 / 出手 / 跳過 / 命中率 / ROI / 總盈虧 / 綜合分數 / 等級
  - 出手分佈（H / D / A 各命中率）
  - 各層觸發場次及佔比
- **不影響**遊戲進度與排行榜數據
- **原始數據**計算，**不經 ±5% 抖動**

### 🏆 排行榜
- **Top 10 迷你榜**（嵌在主頁底部）
- **Top 100 完整榜**（彈窗顯示）
- 玩家完成 50 場後可 **📤 上傳成績**（名字 / 綜合分數 / 命中率 / ROI / 盈虧 / 場次）
- **Tier 由前端根據分數即時計算**（不上傳 tier，日後調門檻自動套用）
- **過濾機制**：只顯示 0 ~ 100 分的合法紀錄，> 100 視為作弊自動隱藏
- 通過 Google Apps Script API 實時讀寫
- **更新時機**：首次進入 / 玩家上傳後 / 手動點「🔄 重新載入」

### 📊 歷史數據統計
- 實時讀取 Google Sheets 數據
- 每 **15 秒** 自動同步
- 顯示：總盈虧 / 命中數 / 總成本 / 出手數 / ROI / 命中率 / 資料庫更新日期
- 讀取位置：`L7`～`L12` + `M2`（更新日期）

### 🎨 UI / UX
- 🌙 / ☀️ **深淺色主題**（localStorage 記憶）
- 🌐 **三語言**：繁中 / 簡中 / 英文（完整覆蓋所有按鈕、提示、開發者面板）
- 滾動時頂部按鈕自動淡出
- 玻璃擬態（Glassmorphism）設計
- 綜合分數**獨立大字顯示**（含公式明細）

### ⚙️ 開發者模式（隱藏）
- 密碼解鎖（預設 `football`）
- **⚙️ 系統設定**：彈出式面板，修改 **14 層公式參數**
- **🔄 重置遊戲**：一鍵清空遊戲進度
- 套用後自動收起，Toast 提示成功
- **📚 資料庫資訊**：實時顯示載入的真實比賽場數

---

## 🚀 快速開始

### 方法 1：單檔案

下載 `index.html`，用瀏覽器打開即可。

```bash
git clone https://github.com/thevker/FootBall-AI.git
cd FootBall-AI
# 用瀏覽器打開 index.html
```

### 方法 2：本地伺服器

```bash
# Python
python -m http.server 8000

# Node.js
npx serve
```

然後瀏覽 `http://localhost:8000`

### 方法 3：部署到 GitHub Pages

1. 將 `index.html` 推到 GitHub repo
2. 進入 **Settings → Pages**
3. Source 選 `main` branch
4. 網址：`https://thevker.github.io/FootBall-AI/`

---

## 📐 核心公式（14 層）

| 層 | 條件 | 結果 |
|---|---|---|
| 1 | `B≥32` 且 `\|A−C\|≤6` | **D**（買和）|
| 2 | `A≥60` 且 `C≤11` 且 `140≤D≤190` 且 `400≤F≤480` | **H**（買主）|
| 3 | `\|A−C\|≤3` 且 `E<380` 且 `\|D−F\|<40` | **D**（買和）|
| 4 | `A≥45` 且 `C≤20` 且 `\|D−F\|<70` 且 `D<400` | **D**（買和）|
| 5 | `\|D−F\|<18` | **D**（買和）|
| 6 | `A≥42` 且 `155≤D<205` 且 `D≠F` 且 `F>D` 且 `\|A−C\|≥50` | **D**（買和）|
| 7 | `A≥42` 且 `155≤D<205` 且 `D≠F` | **H**（買主）|
| 8 | `A≥36` 且 `205<D≤235` 且 `D≠F` | **D**（買和）|
| 9 | `D≥340` 且 `A≥40` 且 `F<250` 且 `D>F` | **D/A**（見下）|
| 10 | `C>A` 且 `500≤F≤550` 且 `D<200` | **D**（買和）|
| 11 | `C>A` 且 `F>D` 且 `F<550` 且 `E>300` | **H**（反向買主）|
| 12 | `C>A` 且 `185≤F≤215` | **A**（買客）|
| 13 | `C>A` 且 `F>D` 且 `F<300` 且 `C<45` 且 `D<250` | **D**（買和）|
| 14（兜底）| 賠率博弈 | 見下 |

**第 9 層細分：**
```
D≥340 且 A≥40 且 F<250 且 D>F：
  ├─ B≥28 且 F<150 → D
  ├─ F<200 → A
  └─ 其餘 → D
```

**兜底層（第 14 層）：**
```
D>F：
  ├─ D≥1500：C≥50 → A；A>C → D；否則 skip
  └─ 其餘：A≥33 且 D≥350 → D；否則 H

F>D：
  ├─ F≥700：A≥50 → H；C>A → D；否則 skip
  └─ 其餘：A≥50 且 D≤140 → H；否則 A

D=F：A>C → H；C>A → A；否則 skip
```

**欄位定義（Google Sheets A2:H 逐行）：**

| 欄 | 內容 |
|---|---|
| A | 主勝率（%）|
| B | 和勝率（%）|
| C | 客勝率（%）|
| D | 主賠（×100，例如 158 = 1.58）|
| E | 和賠（×100）|
| F | 客賠（×100）|
| G | 比分（例如 2:1）|
| H | 賽果（H / D / A）|

---

## 🏅 Tier 等級門檻（0 ~ 100 分）

| 綜合分數 | 等級 | 顏色 |
|---|---|---|
| ≥ 85 | **EX** | 🟣 紫（發光呼吸）|
| 81 ~ 84.99 | **S+** | 🟡 金 |
| 77 ~ 80.99 | **S** | 🟡 金 |
| 73 ~ 76.99 | **S-** | 🟡 金 |
| 69 ~ 72.99 | **A+** | 🔵 冰藍 |
| 65 ~ 68.99 | **A** | 🔵 冰藍 |
| 61 ~ 64.99 | **A-** | 🔵 冰藍 |
| 57 ~ 60.99 | **B+** | 🟢 淺綠 |
| 53 ~ 56.99 | **B** | 🟢 淺綠 |
| 49 ~ 52.99 | **B-** | 🟢 淺綠 |
| 45 ~ 48.99 | **C+** | 🔴 紅 |
| 41 ~ 44.99 | **C** | 🔴 紅 |
| 37 ~ 40.99 | **C-** | 🔴 紅 |
| 33 ~ 36.99 | **D+** | ⚪ 灰 |
| 29 ~ 32.99 | **D** | ⚪ 灰 |
| 25 ~ 28.99 | **D-** | ⚪ 灰 |
| 21 ~ 24.99 | **E+** | 🟤 啡 |
| 15 ~ 20.99 | **E** | 🟤 啡 |
| 0 ~ 14.99 | **E-** | 🟤 啡 |

**綜合分數公式：**
```
綜合分數 = min(100, 命中率) × 50% + min(100, ROI) × 100%
分數上限封頂 100.00
```
- ROI 負值視為 0，不扣分
- 分數上限 100.00（避免爆表）

---

## 📁 檔案結構

```
FootBall-AI/
├── index.html          # 完整單檔案應用
├── README.md           # 本文件
├── LICENSE             # MIT License
└── screenshots/
    ├── dark-mode.png
    ├── light-mode.png
    ├── tier-example.png
    ├── combo-streak.png
    └── simulation.png
```

---

## 🛠️ 技術棧

| 技術 | 用途 |
|---|---|
| **HTML5** | 頁面結構 |
| **CSS3** | 樣式、動畫、主題變數 |
| **Vanilla JavaScript** | 邏輯、狀態管理 |
| **Google Sheets gviz API** | 實時讀取歷史數據與賽事 |
| **Google Apps Script** | 排行榜讀寫 API |
| **localStorage** | 主題偏好 + 參數記憶 |
| **CSS Keyframes** | Tier 動畫、連勝火焰、升降箭頭、EX 發光 |

**零依賴** — 唔需要 npm、webpack、任何框架。

---

## 🔧 自訂

### 修改 Google Sheets 數據源

搵到 `index.html` 內：

```javascript
const SHEET_ID = '你的_GOOGLE_SHEET_ID';
const SHEET_NAME = '工作表1';
```

改成你嘅 Sheet ID 同工作表名稱。Sheet 需設為「**任何人可檢視**」。

### 修改排行榜 API

搵到 `index.html` 內：

```javascript
var LEADERBOARD_API = '你的_APPS_SCRIPT_URL';
```

改成你部署的 Apps Script Web App URL。

### 修改公式參數

**方法 A**：解鎖開發者模式（點「🔒 開發者模式」→ 輸入密碼 `football`），點「⚙️ 系統設定」彈出面板調整。

**方法 B**：直接改 `index.html` 內的 `PARAMS`：

```javascript
var PARAMS = {
  // Layer 1: 和勝率高 + 主客接近 → 買和
  p1_cbmin: 32, p1_cgap: 6,
  // Layer 2: 主強 + 客極弱 + 主賠中低 + 客賠中高 → 買主
  p2_hmin: 60, p2_cmax: 11, p2_dmin: 140, p2_dmax: 190, p2_fmin: 400, p2_fmax: 480,
  // Layer 3: 勝率差 + 和賠低 + 主客賠近 → 買和
  p3_wgap: 3, p3_emax: 380, p3_ogap: 40,
  // Layer 4: 主強 + 客弱 + 主客賠近 + 主賠中 → 買和
  p4_hmin: 45, p4_cmax: 20, p4_ogap: 70, p4_dmax: 400,
  // Layer 5: 主客賠差小 → 買和
  p5_ogap: 18,
  // Layer 6: 主強 + 客賠高 + 勝率差極大 → 買和
  p6_hmin: 42, p6_dmin: 155, p6_dmax: 205, p6_wgap: 50,
  // Layer 7: 主強 + 主賠低中 → 買主
  p7_hmin: 42, p7_dmin: 155, p7_dmax: 205,
  // Layer 8: 主強 + 主賠中 → 買和（A≥36）
  p8_hmin: 36, p8_dmin: 205, p8_dmax: 235,
  // Layer 9: 主賠極高 + 主強 + 客賠低 → 買和（含極低買客）
  p9_dmin: 340, p9_hmin: 40, p9_fmax: 250, p9_low: 200, p9_bmin: 28, p9_fverylow: 150,
  // Layer 10: 客強 + 客賠極高 + 主賠低 → 買和
  p10a_fmin: 500, p10a_fmax: 550, p10a_dmax: 200,
  // Layer 11: 客強客冷 → 反向買主
  p10_fmax: 550, p10_emin: 300,
  // Layer 12: 客強 + 客賠價值 → 買客
  p11_fmin: 185, p11_fmax: 215,
  // Layer 13: 客略強 + 客賠中 + 客勝率低 + 主賠低 → 買和
  p12_cmax: 45, p12_fmax: 300, p12_dmax: 250,
  // Layer 14: 賠率博弈（兜底）
  pd_skip: 1500, pd_cAmin: 50,
  pb_hmin: 33, pb_dmin: 350, pb_fskip: 700, pb_hAmin: 50,
  pb_honly: 50, pb_donly: 140
};
```

### 修改 Tier 分佈

搵到 `function getTier(rate)`，目前分佈為 **19 級**：

```javascript
function getTier(rate) {
  if (rate >= 85)   return { tier:'EX', descKey:'tierEX' };
  if (rate >= 81)   return { tier:'S+', descKey:'tierS' };
  if (rate >= 77)   return { tier:'S',  descKey:'tierS' };
  if (rate >= 73)   return { tier:'S-', descKey:'tierS' };
  if (rate >= 69)   return { tier:'A+', descKey:'tierA' };
  if (rate >= 65)   return { tier:'A',  descKey:'tierA' };
  if (rate >= 61)   return { tier:'A-', descKey:'tierA' };
  if (rate >= 57)   return { tier:'B+', descKey:'tierB' };
  if (rate >= 53)   return { tier:'B',  descKey:'tierB' };
  if (rate >= 49)   return { tier:'B-', descKey:'tierB' };
  if (rate >= 45)   return { tier:'C+', descKey:'tierC' };
  if (rate >= 41)   return { tier:'C',  descKey:'tierC' };
  if (rate >= 37)   return { tier:'C-', descKey:'tierC' };
  if (rate >= 33)   return { tier:'D+', descKey:'tierD' };
  if (rate >= 29)   return { tier:'D',  descKey:'tierD' };
  if (rate >= 25)   return { tier:'D-', descKey:'tierD' };
  if (rate >= 21)   return { tier:'E+', descKey:'tierE' };
  if (rate >= 15)   return { tier:'E',  descKey:'tierE' };
  return { tier:'E-', descKey:'tierE' };
}
```

### 修改 Tier 顏色

搵到 `var TIER_FAMILY_COLORS = {...}`：

- `EX` → 紫（深紫背景 + 亮紫文字 + 發光呼吸特效）
- `S` → 金
- `A` → 冰藍
- `B` → 淺綠
- `C` → 紅
- `D` → 灰
- `E` → 啡

### 修改 Tier 顯示門檻

```javascript
var TIER_MIN_PLAYED = 5;           // 玩幾場才顯示 Tier
var TIER_WEIGHT_HITRATE = 0.5;     // 命中率權重
var TIER_WEIGHT_ROI = 1.0;         // ROI 權重
var MAX_PLAYS = 50;                // 挑戰上限場次
```

### 修改跳過次數

搵到 `function getMaxSkips()`：

```javascript
function getMaxSkips() {
  return 2 + Math.floor(gameState.played / 10);
  //      ↑ 預設次數    ↑ 每 N 場 +1 次
}
```

### 修改防作弊微調範圍

搵到 `function jitterMatchData(m)`，核心抖動邏輯：

```javascript
newHw = m.hw + signH * randRange(0, 2);      // 勝率 ±2%
newHo = m.ho * (1 + signH * randRange(0, 0.01));  // 賠率 ±1%
newDoo = m.doo * (1 + randRange(-0.01, 0.01));
```

將 `0.01` 改成 `0.03` 即為 ±3%；改成 `0.05` 即為 ±5%。

---

## 📋 使用流程

```
1. 開啟網頁
   ↓
2. 閱讀條款（滾到底）→ 按「我已閱讀並同意」
   ↓
3. 進入主頁面
   ├─ 頂部：歷史數據統計（每 15 秒自動同步）
   ├─ 中間：智能預測計算器
   ├─ 底部：猜賽果挑戰（讀取真實數據）+ Top 10 排行榜
   └─ 模擬測試按鈕（開發者模式下可配合調參使用）
   ↓
4. 輸入 6 個數據 → 按「計算結果」→ 得出建議 + EV
   ↓
5. 玩猜賽果累積 Tier 等級、觸發連勝特效
   ↓
6. 玩滿 50 場 → 上傳成績到排行榜
   ↓
7. （可選）解鎖開發者模式調整公式參數 → 按「🧪 模擬測試」驗證
```

---

## ⚠️ 風險聲明

| 提醒 | 說明 |
|---|---|
| ⚠️ **歷史不等於未來** | 回測表現不代表未來必贏 |
| ⚠️ **樣本量關鍵** | 少於 30 場數字不可信 |
| ⚠️ **勿過度擬合** | 頻繁調參數會失效 |
| ⚠️ **固定注碼** | 唔好因短期黑單加注 |
| ⚠️ **娛樂為主** | 數據分析嘅樂趣，非賺錢捷徑 |

> 本系統及所有相關數據、圖表與分析結果，**僅供學術研究、數據分析及個人興趣之用**，不構成任何形式的投資建議或博彩邀約。
>
> 博彩涉及風險，請嚴格控制注碼，切勿沉迷賭博。

---

## 🤝 貢獻

歡迎提交 Issue 或 Pull Request：

1. Fork 呢個 repo
2. 建立 feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit 你嘅改動 (`git commit -m 'Add some AmazingFeature'`)
4. Push 到 branch (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

---

## 📄 License

本項目基於 **MIT License** 開源 — 詳見 [LICENSE](LICENSE) 檔案。

---

## 👤 作者

**thevker**
- GitHub: [@thevker](https://github.com/thevker)
- Email: your.email@example.com

---

## ⭐ Star History

如果呢個項目對你有幫助，請俾個 ⭐ Star 支持一下！

---

## 📌 免責聲明

```
本軟件按「現狀」提供，不附帶任何明示或暗示的保證。
作者不對使用本軟件所產生嘅任何直接或間接損失負責。
使用前請仔細閱讀系統內嘅「使用守則與風險聲明」。
```

---

<div align="center">

**⚽ 理性參與，享受數據分析嘅樂趣 ⚽**

Made with ❤️ by [thevker]

</div>
