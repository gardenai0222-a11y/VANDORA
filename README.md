# 🏛️ VANDORA ‧ 地政稅務 ＆ 房產估價智庫旗艦工作台

> **開拓 ‧ 落地 ‧ 富饒** ｜ 專為台灣代書、地政士、房仲菁英、不動產投資人與土地所有權人量身打造的極速專業試算工作台。

[![Weekly Real Estate Data Auto-Updater](https://github.com/gardenai0222-a11y/VANDORA/actions/workflows/update_real_estate_weekly.yml/badge.svg)](https://github.com/gardenai0222-a11y/VANDORA/actions/workflows/update_real_estate_weekly.yml)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-brightgreen)](https://gardenai0222-a11y.github.io/VANDORA/)
[![Compliance](https://img.shields.io/badge/Google%20AdSense-Ready-blue)](https://gardenai0222-a11y.github.io/VANDORA/ads.txt)
[![Data Engine](https://img.shields.io/badge/Data-MOI%20OpenData%20%2B%20HPI-orange)](https://data.gov.tw/)

---

## 🌟 核心功能模組

1. **🏡 全國房屋估價與土地行情模型 (`index.html`)**
   - 涵蓋全台 22 縣市、368 鄉鎮市區，即時聯動內政部實價登錄開放資料與信義/清華安信房價指數 (HPI)。
   - 支援透天、大樓、公寓、農地、建地、工業地多元標的之折舊、樓層加成、臨路寬度、土地容積價值科學定價。

2. **⚖️ 地政稅務 ＆ 產權精算旗艦平台 (`tax.html`)**
   - **房地合一稅 2.0**：精算持有年限稅率 (45%、35%、20%、15%)、自住房地 400 萬免稅額與 10% 優惠稅率、重購退稅資格自動檢驗。
   - **土地法第 34 條之 1 處分審查**：共有土地人數過半與持分過半門檻自動判讀、存證信函通知期限追蹤、提存法院要件指引。
   - **遺產稅與贈與稅精密估算**：包含免稅額、扣除額、累進差額與農地農用免稅試算。

3. **📈 置產獲利 ＆ 脫手決策試算 (`roi.html`)**
   - 購屋全週期現金流折現、本息攤還月供、實質租金淨投報率 (Cap Rate)。
   - 轉售資本利得、稅賦扣除後之年化複合報酬率 (IRR) 與最佳出場時機決策分析。

4. **📚 代書實務筆記 ＆ 智庫問答 (`notes.html`)**
   - 精選數十組地政士高頻爭議實務 QA、產權分割技巧、借名登記返還風險、買賣過戶規費清單。

5. **🛡️ 關於我們與合規聲明 (`about.html` / `privacy.html`)**
   - 完整遵守 Google AdSense、GDPR 與台灣個資法合規政策，提供完整的 Cookie 宣告與免責聲明。

---

## 🔄 全自動數據更新管線 (GitHub Actions)

本專案建置完全自動化的每週數據同步管線 (`.github/workflows/update_real_estate_weekly.yml`)：
- **排程時間**：每週一 UTC 03:00 (台灣時間 11:00) 自動觸發。
- **爬蟲核心**：`update_real_estate_data.py` 自動連線「中華民國政府資料開放平台 (data.gov.tw)」與官方房價指數端點。
- **自動校驗**：科學重置 368 行政區行情走勢特徵，自動維護 `sitemap.xml` 爬蟲索引日期與全站快取標籤（Cache-Busting）。
- **零人工介入**：自動 Commit 與 Push 更新，靜態站點秒級重新發布。

---

## 🚀 部署指引 (Deploy to GitHub Pages)

1. 在 GitHub 建立新 Repository（例如：`gardenai0222-a11y.github.io`）。
2. 在本機專案目錄執行下列指令：
   ```bash
   git init
   git add .
   git commit -m "Initial release: VANDORA Real Estate & Land Tax Engine"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
3. 前往 GitHub 倉庫的 **Settings -> Pages**：
   - **Source** 選擇 `Deploy from a branch`。
   - **Branch** 選擇 `main` / `/(root)`，點擊 **Save**。
4. 部署完成後即可直接連線網站！

---

## 📄 著作權與授權條款

© 2026 VANDORA 保留所有權利。所有試算工具僅供產權規劃與稅務估算之輔助參考，實際稅額以各地稅捐稽徵處及地政事務所核定為準。
