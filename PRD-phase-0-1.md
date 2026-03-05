# Project SYNC — Phase 0 & Phase 1 產品需求文件（PRD）

## v1.0 ｜ 2026 年 3 月 5 日

---

## 文件資訊

| 欄位 | 內容 |
|------|------|
| 產品名稱 | Project SYNC — AI 驅動全人健康守護計畫 |
| 文件版本 | v1.0 |
| 負責人 | Soking / 黃仁穩醫師 |
| 涵蓋範圍 | Phase 0（概念驗證）+ Phase 1（MVP） |
| 時間跨度 | 2026 Q1 — 2026 Q3 |
| 參考文件 | [產品路線圖 v3.0](./product-roadmap.md) ｜ [募資評估報告](./fundraising-evaluation.md) ｜ [代幣經濟白皮書](./tokenomics.md) |

---

## 一、產品目標與成功定義

### 1.1 一句話目標

**讓慢性病患者的醫囑落實率從 20% 提升至 60%，透過 AI 行為處方箋 + 遊戲化微任務 + 社區連結。**

### 1.2 Phase 0 成功定義（2026/03 — 04）

| 成功標準 | 可量化指標 |
|---------|----------|
| Google.org 提案送出 | 2026/04/03 前完成 |
| 取得醫療端合作意向 | ≥ 1 封 LOI |
| 可展示的產品原型 | LINE Bot 互動 Demo |
| 驗證使用者需求 | ≥ 5 份病患/家屬訪談紀錄 |
| 募資基礎文件完備 | Pitch Deck + 財務預測 |

### 1.3 Phase 1 成功定義（2026 Q2 — Q3）

| 成功標準 | 可量化指標 |
|---------|----------|
| 行為處方箋完成率 | ≥ 60%（對照組 < 20%） |
| 試辦病患數 | ≥ 50 人 |
| 月活用戶留存率 | ≥ 40% |
| 醫師持續使用率 | ≥ 80% |
| 種子活水夥伴 | ≥ 2 組參與試行 |

---

## 二、使用者角色定義

### 2.1 主要使用者

#### P1：慢性病患者（Primary User）

```
人物誌：陳伯伯，62 歲
- 二型糖尿病 + 高血壓，每 3 個月回診
- 醫師叮囑每天走路、控制飲食，但出了診間就忘
- 有 LINE，會看孫子傳的照片，但不太會用複雜 App
- 住社區附近有銀髮據點，偶爾去但沒有規律
- 最大動力：不想麻煩家人、想看到數字變好
```

**需求：**
- 簡單明確的每日任務提醒（不要太複雜）
- 看得到自己的進步（數字、連續天數）
- 和鄰居一起做比較有動力
- 做了有回饋（哪怕是一句鼓勵的話）

**限制：**
- 不會下載 App（只用 LINE）
- 不理解「Token」「區塊鏈」等概念
- 視力可能不好（字要大）
- 對隱私敏感但不知道如何保護

#### P2：主治醫師（Prescriber）

```
人物誌：黃醫師，45 歲
- 家醫科 / 內科主治醫師
- 每天看 40-60 個病人，每人 5-10 分鐘
- 知道病人回家不會照做，但沒有好工具追蹤
- 希望有 P4P 論質計酬的客觀佐證
- 對新工具有興趣但沒時間學複雜系統
```

**需求：**
- 30 秒內能開出行為處方箋（不能佔用門診時間）
- 下次回診時看到病人行為數據摘要
- P4P 申報有數據佐證
- 不需要自己操作太多東西

**限制：**
- 門診時間極短
- HIS 系統各家不同
- 不願意為了一個新工具改變看診流程

### 2.2 次要使用者

#### P3：社區據點工作人員

- 銀髮據點、社區活動中心的工作人員
- 負責簽到、帶活動、回報參與
- 需要簡單的管理介面

#### P4：家屬 / 照顧者

- 遠距關心長輩的健康行為
- 想知道「今天有沒有出門走路」
- 不想侵犯隱私但想被通知異常

#### P5：種子活水夥伴（Phase 1 後期）

- 2-3 組早期合作的活動舉辦者或在地商家
- 願意提供小額兌換獎勵（如藥局折扣、社區餐廳優惠）
- 需要簡單的任務建立介面

---

## 三、Phase 0 產品需求

### 3.1 LINE Bot Demo（P0-MVP）

**目的：** 展示 AI 行為處方箋的核心互動流程，作為 Google.org 提案的產品佐證。

**不是：** 完整可用的產品。可以是規則式回覆 + 部分 AI 生成。

#### 3.1.1 核心互動流程

```
使用者加入好友
    │
    ▼
歡迎訊息 + 簡短自我介紹
「嗨！我是你的健康夥伴小 SYNC 🏥」
「醫師開了一份專屬你的健康任務，我來幫你一步步完成」
    │
    ▼
每日任務推播（固定時間，如早上 8:00）
「早安！今天的任務：飯後散步 15 分鐘 🚶」
「完成後跟我說一聲，我幫你記錄」
    │
    ▼
使用者回報完成
「走完了！」→ AI 回應 + hEXP 記錄
「太棒了！+10 hEXP ✨ 你已經連續 3 天達標了！」
    │
    ▼
每週摘要
「本週成績：步行 5/7 天、社區活動 1 次、hEXP 累計 85」
「下週繼續，你離下一個里程碑只差 15 分了 💪」
```

#### 3.1.2 Demo 需支援的對話場景

| 場景 | 觸發方式 | 回應 |
|------|---------|------|
| 首次加入 | 加好友 | 歡迎訊息 + 引導設定 |
| 每日任務提醒 | 定時推播 | 今日任務 + 鼓勵語 |
| 完成回報 | 使用者輸入「完成」「走了」等 | 積分記錄 + 連續天數 |
| 查看進度 | 使用者輸入「進度」「我的成績」 | hEXP 總覽 + 本週摘要 |
| 社區活動提醒 | 定時推播（週一） | 本週社區活動清單 |
| 問健康問題 | 自由輸入 | AI 衛教回答（Gemini） |
| 查看排行 | 使用者輸入「排名」 | 匿名化社區排行榜 |

#### 3.1.3 技術規格

| 項目 | 規格 |
|------|------|
| 平台 | LINE Messaging API |
| 語言 | TypeScript / Node.js |
| AI 引擎 | Gemini API（衛教對話） |
| 資料儲存 | Supabase（使用者狀態、hEXP 紀錄） |
| 部署 | Zeabur（與 soking.cc 同平台） |
| 推播機制 | LINE Push API + cron job |

#### 3.1.4 Demo 不需要的功能

- ❌ 穿戴裝置整合（Phase 1）
- ❌ 真實健康存摺 SDK 對接（Phase 1）
- ❌ 完整積點兌換系統（Phase 1）
- ❌ 任務編輯器（Phase 2）
- ❌ 區塊鏈/Token（Phase 3）

### 3.2 提案支援文件

| 文件 | 狀態 | 說明 |
|------|------|------|
| 產品架構白皮書 | ✅ 完成 | project-SYNC-guide.md |
| 產品路線圖 | ✅ 完成 | product-roadmap.md v3.0 |
| 代幣經濟白皮書 | ✅ 完成 | tokenomics.md |
| TW DIW 技術評估 | ✅ 完成 | TW-DIW-evaluation-report.md |
| 募資評估報告 | ✅ 完成 | fundraising-evaluation.md |
| 互動式視覺化網頁 | ✅ 完成 | GitHub Pages |
| TAM/SAM/SOM 一頁摘要 | 🔲 待完成 | — |
| 競品分析矩陣 | 🔲 待完成 | — |
| 3 年財務預測 | 🔲 待完成 | — |
| Demo 影片（2 分鐘） | 🔲 待完成 | LINE Bot 互動錄影 |
| 醫療端 LOI | 🔲 待取得 | 黃仁穩醫師負責 |
| 使用者訪談紀錄 | 🔲 待執行 | 5-10 份 |

---

## 四、Phase 1 產品需求

### 4.1 系統架構總覽

```
┌─────────────────────────────────────────────────────────┐
│                    使用者端（LINE Bot）                    │
│                                                         │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌─────────┐ │
│  │ 任務推播  │  │ 完成回報  │  │ 進度查看  │  │ AI 對話  │ │
│  └─────┬────┘  └─────┬────┘  └─────┬────┘  └────┬────┘ │
└────────┼─────────────┼─────────────┼────────────┼──────┘
         │             │             │            │
    ┌────▼─────────────▼─────────────▼────────────▼──────┐
    │                   API 服務層                         │
    │                                                     │
    │  ┌────────────┐  ┌────────────┐  ┌───────────────┐  │
    │  │ 任務引擎    │  │ 積點引擎    │  │ AI 代理人      │  │
    │  │ (Task)     │  │ (Points)   │  │ (Gemini API)  │  │
    │  └─────┬──────┘  └─────┬──────┘  └───────┬───────┘  │
    └────────┼───────────────┼─────────────────┼──────────┘
             │               │                 │
    ┌────────▼───────────────▼─────────────────▼──────────┐
    │                   資料層                              │
    │                                                     │
    │  ┌────────────┐  ┌────────────┐  ┌───────────────┐  │
    │  │ Supabase   │  │ 健康存摺    │  │ 穿戴裝置      │  │
    │  │ (主資料庫)  │  │ SDK        │  │ API           │  │
    │  └────────────┘  └────────────┘  └───────────────┘  │
    └─────────────────────────────────────────────────────┘

    ┌─────────────────────────────────────────────────────┐
    │                   管理端（Web Dashboard）              │
    │                                                     │
    │  ┌──────────┐  ┌──────────┐  ┌──────────────────┐   │
    │  │ 醫師端    │  │ 據點端    │  │ 活水夥伴端（簡易）│   │
    │  │ 處方管理  │  │ 簽到管理  │  │ 任務建立        │   │
    │  └──────────┘  └──────────┘  └──────────────────┘   │
    └─────────────────────────────────────────────────────┘
```

### 4.2 功能清單與優先序

#### Must-Have（P0 — 必須交付）

| # | 功能 | 使用者 | 說明 |
|---|------|--------|------|
| F1 | **行為處方箋開立** | 醫師 | 在 Web Dashboard 選擇預設模板 + 調整參數，30 秒內完成 |
| F2 | **每日任務推播** | 病患 | LINE 定時推送今日任務，AI 根據處方內容個人化措辭 |
| F3 | **任務完成回報** | 病患 | LINE 對話回報（文字/圖片）+ 穿戴裝置自動偵測 |
| F4 | **hEXP 累計與查看** | 病患 | 累計經驗值、連續天數、等級進度，LINE 圖卡呈現 |
| F5 | **AI 衛教對話** | 病患 | 自由問答，Gemini 根據病患條件（病種、處方）回應 |
| F6 | **回診摘要報告** | 醫師 | 病患行為數據自動彙整，醫師端 Dashboard 可查看 |
| F7 | **社區據點簽到** | 病患 + 據點 | QR Code 簽到，自動記錄出席並發放 hEXP |

#### Should-Have（P1 — 盡量交付）

| # | 功能 | 使用者 | 說明 |
|---|------|--------|------|
| F8 | **兌換積點系統** | 病患 | hEXP 達標後可轉換為兌換積點，在合作商家使用 |
| F9 | **社區活動推薦** | 病患 | AI 根據病患狀態推薦本週合適的社區活動 |
| F10 | **病友互動** | 病患 | 匿名化排行榜 + 簡單的鼓勵互動（按讚） |
| F11 | **家屬通知** | 家屬 | 可訂閱長輩的週摘要（需長輩授權） |
| F12 | **活水夥伴簡易任務建立** | 活水夥伴 | 種子夥伴可在 Dashboard 建立兌換獎勵任務 |

#### Nice-to-Have（P2 — 有了更好）

| # | 功能 | 使用者 | 說明 |
|---|------|--------|------|
| F13 | 穿戴裝置自動同步 | 病患 | Google Fit / Apple Health 數據自動匯入 |
| F14 | 健康存摺 SDK 對接 | 系統 | 匯入病患健保就醫紀錄 |
| F15 | P4P 數據匯出 | 醫師 | 符合健保申報格式的行為佐證報表 |

### 4.3 核心功能詳細規格

#### F1：行為處方箋開立

**使用者：** 醫師（P2）

**流程：**

```
醫師登入 Dashboard
    │
    ▼
選擇病患（搜尋姓名/ID）
    │
    ▼
選擇處方模板
  ├── 糖尿病標準處方（步行 + 飲食 + 回診）
  ├── 高血壓標準處方（運動 + 減鹽 + 量血壓）
  ├── 社交處方（社區活動 + 病友互動）
  └── 自訂處方
    │
    ▼
調整參數
  ├── 每日步行目標（預設 3000 步，可調整）
  ├── 任務頻率（每日/每週/指定天）
  ├── 處方有效期（預設 90 天）
  └── 特殊備註（給 AI 的 context）
    │
    ▼
確認開立 → 系統自動推送至病患 LINE
```

**處方模板資料結構：**

```json
{
  "prescriptionId": "rx-2026-001",
  "patientId": "patient-xxx",
  "doctorId": "doctor-xxx",
  "template": "diabetes-standard",
  "createdAt": "2026-05-15T10:30:00Z",
  "validUntil": "2026-08-15T10:30:00Z",
  "tasks": [
    {
      "type": "daily-walk",
      "target": 3000,
      "unit": "steps",
      "frequency": "daily",
      "hexpReward": 10,
      "verification": "wearable"
    },
    {
      "type": "diet-record",
      "frequency": "daily",
      "hexpReward": 5,
      "verification": "self-report"
    },
    {
      "type": "community-activity",
      "frequency": "weekly",
      "minPerWeek": 1,
      "hexpReward": 15,
      "verification": "qr-checkin"
    }
  ],
  "aiContext": "患者血糖控制不佳，HbA1c 8.2，需加強飲食控制",
  "status": "active"
}
```

**驗收標準：**
- 醫師可在 30 秒內完成開立
- 系統自動推送歡迎訊息至病患 LINE
- 處方內容正確映射為每日任務推播排程

#### F2：每日任務推播

**使用者：** 病患（P1）

**推播時機與內容：**

| 時段 | 觸發條件 | 訊息類型 |
|------|---------|---------|
| 早上 8:00 | 每日固定 | 今日任務清單 + 鼓勵語 |
| 中午 12:00 | 若上午未回報任何任務 | 溫和提醒 |
| 下午 17:00 | 若社區活動當天有排程 | 活動提醒 |
| 晚上 20:00 | 若當天有完成任務 | 每日總結 + 明日預告 |
| 不推播 | 週日（可設定休息日） | — |

**訊息個人化規則：**
- AI 根據處方中的 `aiContext` 調整措辭
- 連續達標時加入鼓勵語（「連續 7 天！太厲害了」）
- 中斷時溫和喚回（「好幾天沒見到你了，今天一起走走？」）
- 不使用專業術語（不說「hEXP」，說「健康分數」）

**訊息格式（LINE Flex Message）：**

```
┌──────────────────────────┐
│ 🌅 早安，陳伯伯！          │
│                          │
│ 今天的健康任務：            │
│                          │
│ 🚶 飯後散步 15 分鐘        │
│    目標：3000 步           │
│                          │
│ 📝 記錄午餐吃了什麼        │
│                          │
│ 連續達標：第 5 天 🔥        │
│ 健康分數：85 分            │
│                          │
│ [完成步行] [記錄飲食]      │
└──────────────────────────┘
```

**驗收標準：**
- 推播準時送達（誤差 < 1 分鐘）
- 訊息內容與處方一致
- 快捷按鈕可直接回報完成
- 每日不超過 4 則推播（避免打擾）

#### F3：任務完成回報

**使用者：** 病患（P1）

**回報方式：**

| 方式 | 觸發 | 驗證 |
|------|------|------|
| 按鈕回報 | 點擊 LINE Flex Message 按鈕 | 記錄時間戳 |
| 文字回報 | 輸入「走完了」「完成」等自然語言 | AI 語意辨識 |
| 照片回報 | 拍攝飲食/活動照片 | AI 圖片辨識（輔助） |
| 自動偵測 | 穿戴裝置 API（Phase 1 後期） | 步數/心率資料 |
| QR 簽到 | 社區據點掃碼 | 地點 + 時間驗證 |

**回報後回應：**

```
使用者：「今天走了半小時」

AI：「太棒了！🎉 +10 健康分數
     連續第 5 天達標，再 2 天就解鎖新成就！

     今天的步行加上你上午的太極拳，
     已經完成 2/3 的每日目標了。

     晚餐記得少油少鹽喔 💪」
```

**驗收標準：**
- 自然語言回報辨識準確率 ≥ 90%
- 回報後 3 秒內收到回應
- hEXP 即時更新至使用者帳戶
- 防重複回報（同一任務當天限一次）

#### F4：hEXP 累計與查看

**使用者：** 病患（P1）

**查看介面（LINE Flex Message）：**

```
┌──────────────────────────┐
│ 📊 陳伯伯的健康成績單       │
│                          │
│ ⭐ 健康分數：1,250        │
│ 🏆 等級：Lv.2 健康玩家     │
│ 🔥 連續達標：12 天         │
│                          │
│ ━━━━━━━━━━━━━━ 80%       │
│ 距離 Lv.3 還差 750 分      │
│                          │
│ 📈 本週成績：              │
│   步行 6/7 天 ✅           │
│   飲食紀錄 5/7 天 ✅       │
│   社區活動 1 次 ✅         │
│                          │
│ 💰 可兌換積點：15 點       │
│                          │
│ [查看兌換商品] [分享成績]   │
└──────────────────────────┘
```

**加成機制（使用者感知版本）：**

使用者不需要知道「Streak Multiplier × Diversity Multiplier」，只看到：
- 「連續 7 天 → 分數加倍期開始！」
- 「今天同時走路 + 記飲食 + 參加活動 → 額外獎勵 30%！」

**驗收標準：**
- 數據即時更新（回報後 3 秒內反映）
- 等級進度條直覺易懂
- 大字體、高對比（高齡友善）
- 連續天數中斷時有寬限提示（「還有 6 天寬限期，快回來！」）

#### F6：回診摘要報告

**使用者：** 醫師（P2）

**Dashboard 介面：**

```
┌─────────────────────────────────────────────┐
│ 病患：陳○○  │  處方有效期：2026/05/15 - 08/15  │
│──────────────────────────────────────────────│
│                                             │
│ 📊 行為處方執行摘要                           │
│                                             │
│ 步行達標率：78%（56/72 天）    ████████░░ │
│ 飲食紀錄率：65%（47/72 天）    ██████░░░░ │
│ 社區活動：  8 次（目標 10 次）  ████████░░ │
│ 整體完成率：72%               ███████░░░ │
│                                             │
│ 📈 趨勢：前 4 週穩定上升，第 5 週略降          │
│ ⚠️ 注意：最近 5 天未回報飲食紀錄               │
│                                             │
│ 🏆 hEXP 等級：Lv.2（累計 1,850）             │
│ 🔥 最長連續天數：18 天                        │
│                                             │
│ [查看完整紀錄] [匯出 PDF] [調整處方]           │
└─────────────────────────────────────────────┘
```

**驗收標準：**
- 一眼掌握病患行為摘要（< 10 秒）
- 自動標記異常（如中斷、下降趨勢）
- 可匯出 PDF（附診時使用）
- 支援處方即時調整

#### F7：社區據點簽到

**流程：**

```
據點工作人員開啟 Dashboard → 產生當日 QR Code
    │
    ▼
病患到場 → 用 LINE 掃描 QR Code
    │
    ▼
系統驗證：
  ├── QR Code 是否有效（每 5 分鐘更新）
  ├── 使用者是否有對應處方
  └── 今日是否已簽到
    │
    ▼
簽到成功 → 發放 hEXP + 推播確認
「簽到成功！+20 健康分數 ✨ 今天的太極拳加油！」
    │
    ▼
活動結束後（停留 ≥ 20 分鐘）→ 自動發放活動完成獎勵
「太極拳完成！+15 健康分數 🎉」
```

**驗收標準：**
- 掃碼到確認 < 3 秒
- QR Code 動態更新（防代簽）
- 停留時間驗證（避免掃完就走）
- 據點端可查看今日簽到名單

### 4.4 資料模型

#### Supabase 資料表設計

```sql
-- 使用者
CREATE TABLE sync_users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  line_user_id TEXT UNIQUE NOT NULL,
  display_name TEXT,
  level INTEGER DEFAULT 0,  -- 0-3 (Phase 1)
  total_hexp INTEGER DEFAULT 0,
  exchange_points INTEGER DEFAULT 0,
  streak_days INTEGER DEFAULT 0,
  last_active_date DATE,
  peak_hexp INTEGER DEFAULT 0,  -- 衰減用保底值
  created_at TIMESTAMPTZ DEFAULT now()
);

-- 行為處方箋
CREATE TABLE sync_prescriptions (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  patient_id UUID REFERENCES sync_users(id),
  doctor_id TEXT NOT NULL,
  template TEXT NOT NULL,
  tasks JSONB NOT NULL,
  ai_context TEXT,
  valid_from DATE NOT NULL,
  valid_until DATE NOT NULL,
  status TEXT DEFAULT 'active',  -- active, completed, expired
  created_at TIMESTAMPTZ DEFAULT now()
);

-- 任務紀錄
CREATE TABLE sync_task_records (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES sync_users(id),
  prescription_id UUID REFERENCES sync_prescriptions(id),
  task_type TEXT NOT NULL,
  completed_at TIMESTAMPTZ DEFAULT now(),
  verification_method TEXT,  -- button, text, photo, auto, qr
  hexp_earned INTEGER NOT NULL,
  points_earned INTEGER DEFAULT 0,
  streak_multiplier NUMERIC(3,1) DEFAULT 1.0,
  diversity_multiplier NUMERIC(3,1) DEFAULT 1.0,
  raw_data JSONB,  -- 穿戴裝置原始數據等
  created_at TIMESTAMPTZ DEFAULT now()
);

-- 社區據點
CREATE TABLE sync_venues (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  name TEXT NOT NULL,
  address TEXT,
  contact_person TEXT,
  qr_secret TEXT NOT NULL,  -- 動態 QR 生成用
  created_at TIMESTAMPTZ DEFAULT now()
);

-- 簽到紀錄
CREATE TABLE sync_checkins (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES sync_users(id),
  venue_id UUID REFERENCES sync_venues(id),
  checkin_at TIMESTAMPTZ DEFAULT now(),
  checkout_at TIMESTAMPTZ,
  duration_minutes INTEGER,
  hexp_earned INTEGER,
  created_at TIMESTAMPTZ DEFAULT now()
);

-- 兌換紀錄
CREATE TABLE sync_exchanges (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES sync_users(id),
  partner_id TEXT,  -- 活水夥伴 ID
  item_name TEXT NOT NULL,
  points_spent INTEGER NOT NULL,
  status TEXT DEFAULT 'pending',  -- pending, redeemed, expired
  redeemed_at TIMESTAMPTZ,
  created_at TIMESTAMPTZ DEFAULT now()
);
```

### 4.5 API 端點設計

```
LINE Webhook
  POST /api/sync/line-webhook          LINE 訊息回調

使用者端
  GET  /api/sync/user/profile          取得個人資料 + hEXP + 等級
  GET  /api/sync/user/tasks/today      取得今日任務清單
  POST /api/sync/user/tasks/complete   回報任務完成
  GET  /api/sync/user/stats/weekly     取得週統計
  GET  /api/sync/user/exchange/items   取得可兌換項目
  POST /api/sync/user/exchange         執行兌換

醫師端
  GET  /api/sync/doctor/patients       取得病患清單
  POST /api/sync/doctor/prescription   開立處方箋
  GET  /api/sync/doctor/patient/:id    取得病患行為摘要
  GET  /api/sync/doctor/report/:id     取得回診報告

據點端
  POST /api/sync/venue/qr-generate     產生動態 QR Code
  POST /api/sync/venue/checkin         處理簽到
  GET  /api/sync/venue/today           取得今日簽到清單

推播排程（內部）
  POST /api/sync/cron/daily-push       每日任務推播
  POST /api/sync/cron/weekly-summary   每週摘要
  POST /api/sync/cron/decay-check      hEXP 衰減檢查
```

### 4.6 非功能需求

| 項目 | 規格 |
|------|------|
| 回應時間 | LINE 回覆 < 3 秒 |
| 可用性 | 99.5%（醫療場域不能常當機） |
| 資料備份 | Supabase 自動備份 + 每週手動快照 |
| 隱私合規 | 個資法 + 醫療資料保護（不儲存原始病歷） |
| 字體大小 | LINE Flex Message 內文 ≥ 16px |
| 色彩對比 | WCAG AA 標準（高齡友善） |
| 語言 | 繁體中文，通俗用語（避免醫療/科技術語） |

---

## 五、Phase 1 開發時程

### Sprint 規劃（2 週一個 Sprint）

| Sprint | 時間 | 交付 |
|--------|------|------|
| Sprint 0 | Q2 第 1-2 週 | 環境建置：Supabase schema、LINE Bot 基礎框架、API 骨架 |
| Sprint 1 | Q2 第 3-4 週 | F1 處方開立 + F2 每日推播 + F3 任務回報（核心迴圈） |
| Sprint 2 | Q2 第 5-6 週 | F4 hEXP 系統 + F5 AI 對話 + F7 社區簽到 |
| Sprint 3 | Q2 第 7-8 週 | F6 回診報告 + 整合測試 + 首批病患上線 |
| Sprint 4 | Q3 第 1-2 週 | F8 兌換積點 + F9 社區推薦 + bug 修復 |
| Sprint 5 | Q3 第 3-4 週 | F10 病友互動 + F11 家屬通知 + F12 活水夥伴（簡易） |
| Sprint 6 | Q3 第 5-6 週 | 數據分析 + traction 報告 + Phase 2 準備 |

### 里程碑

```
Q2 第 4 週 ─── MVP 核心迴圈完成（F1-F3）
              可以端對端展示「醫師開處方 → 病患收到任務 → 回報完成」

Q2 第 8 週 ─── Phase 1 v1.0 上線
              首批 ≥ 10 名病患開始使用

Q3 第 2 週 ─── Phase 1 v1.1
              兌換積點 + 社區活動功能加入

Q3 第 6 週 ─── Phase 1 數據收割
              彙整 traction 數據，準備 Phase 2 + 募資用
```

---

## 六、衡量指標與數據收集

### 核心指標（投資人會問的）

| 指標 | 定義 | 收集方式 | 目標 |
|------|------|---------|------|
| 行為處方箋完成率 | 處方期間內完成 ≥ 70% 任務的病患比例 | sync_task_records 統計 | ≥ 60% |
| MAU | 月內至少完成 1 次任務的使用者數 | sync_task_records 去重 | ≥ 50 |
| D7 留存率 | 註冊 7 天後仍活躍的比例 | sync_users + 活躍定義 | ≥ 50% |
| D30 留存率 | 註冊 30 天後仍活躍的比例 | sync_users + 活躍定義 | ≥ 40% |
| 醫師使用率 | 開立處方後 30 天內至少查看 1 次報告的醫師比例 | Dashboard 訪問 log | ≥ 80% |
| 平均每日互動次數 | 每位活躍用戶每日 LINE 互動次數 | LINE webhook log | ≥ 3 次 |
| 社區據點出席率 | 有處方的病患每月至少出席 1 次社區活動的比例 | sync_checkins 統計 | ≥ 30% |

### 輔助指標

| 指標 | 定義 | 用途 |
|------|------|------|
| 任務回報方式分佈 | 按鈕/文字/照片/自動各佔比 | 優化互動設計 |
| 推播開啟率 | LINE 推播被閱讀的比例 | 調整推播時間/頻率 |
| AI 對話滿意度 | 衛教問答後的回饋（有用/沒用） | 優化 AI prompt |
| 中斷原因分析 | 中斷前最後活躍的任務類型/時段 | 改善留存策略 |
| 積點兌換率 | 有積點的用戶中實際兌換的比例 | 驗證獎勵機制 |

---

## 七、風險與依賴

| 風險 | 影響 | 機率 | 緩解 |
|------|------|------|------|
| LINE Bot 審核延遲 | 延後上線時程 | 中 | 提前申請 LINE Official Account + Messaging API |
| Gemini API 政策限制（醫療內容） | AI 對話功能受限 | 中 | 準備 Claude API 作為備案 |
| 合作診間招募不足 | Phase 1 病患數不達標 | 中 | 黃醫師自有診間作為保底 + 擴展至 2-3 家 |
| 高齡使用者上手困難 | 留存率低 | 高 | 設計陪伴式引導 + 據點工作人員協助設定 |
| 穿戴裝置普及率低 | 步行驗證依賴自主回報 | 中 | Phase 1 以自主回報為主，穿戴裝置為加分項 |
| 健康存摺 SDK 申請延遲 | 無法取得健保數據 | 中 | Phase 1 不依賴 SDK，以處方資料為主 |

### 外部依賴

| 依賴 | 預計取得時間 | 替代方案 |
|------|------------|---------|
| LINE Official Account + Messaging API | 申請後 1-2 週 | — |
| Gemini API 使用權限 | 已可申請 | Claude API |
| 合作診間簽約 | Phase 0 期間 | 黃醫師自有診間 |
| 社區據點合作 | Phase 1 Sprint 1-2 | 先以 1-2 個據點試行 |

---

## 八、開放問題

以下問題需在 Phase 1 開發過程中逐步釐清：

| # | 問題 | 影響功能 | 預計決策時間 |
|---|------|---------|------------|
| Q1 | LINE Bot vs. LINE LIFF App？推播限制如何處理？ | F2 推播 | Sprint 0 |
| Q2 | Gemini API 是否允許醫療情境的個人化建議？ | F5 AI 對話 | Sprint 0 |
| Q3 | QR Code 動態更新的最短間隔？5 分鐘是否合理？ | F7 簽到 | Sprint 2 |
| Q4 | 穿戴裝置 API 整合的優先支援品牌？ | F13 自動同步 | Sprint 4 |
| Q5 | 兌換積點的對價比率如何設定？（1 積點 ≈ NT$?） | F8 兌換 | Sprint 4 |
| Q6 | 家屬通知的隱私授權機制如何設計？ | F11 家屬通知 | Sprint 5 |

---

*本文件為 Project SYNC Phase 0 & Phase 1 產品需求文件第一版。*
*隨開發進展將持續更新。*
*最後更新：2026 年 3 月 5 日 ｜ 版本：v1.0*
