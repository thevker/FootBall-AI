# 📊 xG 賽事分析器

> 🔗 **線上使用**：<https://thevker.github.io/FootBall-AI>
> 
> 🎬 **使用教學**：<https://youtube.com/shorts/Xb3Jc_3utFg?si=c_gEf4lHqIbK5nqY>
> 
> 📦 **GitHub Repo**：<https://github.com/thevker/FootBall-AI>
> 
> 👤 **作者**：[@thevker](https://github.com/thevker)
> 

> 基於 xG（預期入球）與得失球數據的足球賽事預測工具，結合狀態、賠率、聯賽排名等多維度指標，提供賽果預測、入球大細及波膽推薦。工具完全免費開放使用！

![Version](https://img.shields.io/badge/version-3.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Data](https://img.shields.io/badge/data-FootyStats-orange)
![Platform](https://img.shields.io/badge/platform-Web-lightgrey)

---

## 📖 目錄

- [項目簡介](#-項目簡介)
- [功能特色](#-功能特色)
- [快速開始](#-快速開始)
- [輸入數據說明](#-輸入數據說明)
- [預測邏輯](#-預測邏輯)
- [實力評級系統](#-實力評級系統)
- [使用流程](#-使用流程)
- [技術細節](#-技術細節)
- [常見問題](#-常見問題)
- [免責聲明](#-免責聲明)

---

## 🎯 項目簡介

**xG 賽事分析器** 是一個單頁式網頁應用（SPA），專為足球賽事分析而設。透過輸入兩隊的 **xG / xGA、場均得分、場均失球、近期狀態、賠率及聯賽排名**，系統會即時計算出預測結果，並支援一鍵截圖保存。

> ⚠️ **工具只作娛樂分析，切勿沉迷賭博。**

---

## ✨ 功能特色

| 功能 | 說明 |
|---|---|
| 🆓 **完全免費** | 無需密碼、無時間限制，打開即用 |
| ⚙️ **標準模式** | 完整功能：輸入所有數據，並顯示賽果預測與六角雷達圖分析 |
| ⚡ **極簡模式** | 快速預測：只需輸入「得分」與「失球」，一鍵得出結果（隱藏分析區塊） |
| 🏆 **多級賽果預測** | 按淨勝球潛力分為主勝、主勝(-1)、主勝(-2) 等讓球級別 |
| ⚽ **三欄入球大細** | 主隊 1.5 / 總入球 2.5 / 客隊 1.5，採雙門檻判斷 |
| 🎲 **5x5 彩色波膽網格** | 以 0:0 至 4:4 的網格呈現，根據「距離」以綠、黃、紅三色顯示可能比分 |
| 📊 **六角雷達圖** | 進攻、防守、狀態、賠率、轉換、排名六維可視化（標準模式限定） |
| 🏅 **等級評分 E~X** | 每項指標換算為百分比並給出 E/D/C/B/A/S/X 等級 |
| 💪 **戰力總評** | 六項指標平均，以「戰力: A (84.8)」斜體粗體顯示 |
| 📸 **雙重保存功能** | 支援「保存預測」（僅截圖預測區）與「保存分析」（僅截圖雷達圖分析區） |
| 📱 **手機優先設計** | 響應式版面，完美適配手機屏幕 |

---

## 🚀 快速開始

### 🔗 線上使用（推薦）

直接打開：

👉 <https://thevker.github.io/FootBall-AI>

### 🎬 使用教學

如果唔清楚點用，可以睇以下短片教學 👇

👉 <https://youtube.com/shorts/Xb3Jc_3utFg?si=c_gEf4lHqIbK5nqY>

### 方式一：本機開啟

1. 將 `index.html` 下載到本機
2. 用任何現代瀏覽器（Chrome / Safari / Edge / Firefox）雙擊開啟即可使用。

### 方式二：Fork 並部署到自己的 Pages

```bash
# 1. Clone 專案
git clone https://github.com/thevker/FootBall-AI.git
cd FootBall-AI

# 2. 推送到自己的 repo 後
# 開啟 Settings → Pages → 選擇分支即可
