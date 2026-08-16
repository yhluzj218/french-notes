# Learning Strategy — 發音優先路線

> 這是整個學習系統的頂層策略。`start today` 出任務時必須對齊目前所在階段。
> 長期目標見 [profile.md](../profile.md)。

## 核心理念

目標**不是**「背 5000 個單字」，而是：

> **任何沒看過的新單字，都能根據 IPA + 法語拼字規則，大約念對 90%。**

達成方式是建立三層能力（由下往上，下層沒穩，上層會歪）：

| 層 | 能力 | 說明 |
|---|---|---|
| 第一層 | 聽得出所有法語音 | 例：/u/ /y/ /ø/ /œ/ /o/ 要能分辨（tout vs tu 只差一個音，意思就不同） |
| 第二層 | 看到 IPA 能發音 | 看到 /pəti/ 立刻念出 petit，不是猜 |
| 第三層 | 看到拼字能預測 IPA | 看到 nation 直接知道 /nasjɔ̃/；一個規則可套用到幾百個字 |

## 學習順序（三階段）

### Phase 1 — 征服所有法語音（約 1 個月，2026-07 起）

- 範圍：母音、鼻母音、半母音、子音、/ʁ/、liaison、e muet（約 40 個 phonemes）
- 每天 20 分鐘，重點是**精準**，不是量
- 訓練到穩定後才進 Phase 2
- 練到的發音規則收進 `10_knowledge_base/pronunciation/`（可重用規則層級）
- 要複習發音（母音/鼻母音/子音）該看哪個檔案 → [pronunciation-review-map.md](pronunciation-review-map.md)；實際每週排程 → [phase1_practice_guide.md](../phase1_practice_guide.md)

### Phase 2 — 拼字→發音規則（約 2 個月）

- 背**規則**不是背字，例如：`eau/au → /o/`、`oi → /wa/`、`ou → /u/`、`eu → /ø/`、`œu → /œ/`、`tion → /sjɔ̃/`
- 每條規則收進 `10_knowledge_base/pronunciation/`，附例字

### Phase 3 — 大量單字

每個新單字走「預測 → 驗證 → 修正」流程，不是直接背意思：

```
看單字（遮住 IPA）
→ 自己念，寫下自己猜的 IPA（不用完全正確）
→ 打開 IPA 驗證
→ 聽真人發音
→ 模仿、錄音
→ AI / 老師比對修正
→ 再念一次
```

## 量化達成標準

| 能力 | 練法 | 達成標準 |
|---|---|---|
| IPA 辨識 | 看 IPA 念音 | 正確率 >95% |
| 拼字→發音 | 看單字直接念 | 正確率 >90% |
| 發音→IPA | 聽音寫 IPA | 正確率 >90% |
| Minimal pairs | tu/tout、peu/peur | 能穩定分辨與發音 |
| 錄音比對 | AI 或老師糾正 | 同一錯誤不重複出現 |

發音錯誤照常走三階段 confidence policy（evidence_log → error_db，Category: `Pronunciation`），這些正確率追蹤先靠練習記錄，不建獨立分數資料庫。

## 與實體課程的對齊（分兩個時期）

使用者有每週六的法語課（課本 + cahier d'activité）。課堂角色依時期不同：

### 時期一：跟課期（2026-07 ~ 2026-09 初，IELTS 備考中）

每週投入約 5–6 小時，**課程進度是主軸**，每日自習跟著老師教到的音素走：

- 老師教過的音素 → 當週每日聽辨/minimal pairs 的練習範圍（例：Lesson 01 教了 11 個母音 → 本週練母音聽辨，見 [voyelles-francaises](../../10_knowledge_base/pronunciation/voyelles-francaises.md)）
- 老師還沒教的音素 → 不搶先自學，等課程教到再納入
- `start today` 出任務時必須讀最近一筆 lesson 筆記，確認：當週音素範圍、作業 deadline、下週預習範圍
- 課程作業（cahier）優先於自主練習任務

### 時期二：換檔期（2026-09 IELTS 考完後）

投入拉到每週 10–12 小時，**自學領跑，課堂降級為複習 + 口說驗證場**：

- 「不搶先自學」規則失效：文法、單字、Phase 2 拼字規則照自己的進度衝，不等課堂
- 課堂價值 = 輸出糾錯（開口、被糾音）+ 間隔複習（已學內容第二次見面）+ 每週進度地板
- cahier 作業照做（會變快變簡單，屬於複習）
- `start today` 出任務以自學進度為主，lesson 筆記只用來確認作業 deadline 和口說驗證重點
- 自學材料：已購線上課程《從0開始學法文｜路易教你旅遊日常會話》第 2 章起（打招呼、自我介紹、數字、日常表達 → 對應 2026-10 milestone；第 3–4 章旅遊/聊天情境隨後）。Phase 1 期間只用其第 1 章音素影片（見 [phase1_practice_guide.md](../phase1_practice_guide.md) 工具⑤）
- 換檔期補充資源（來源：中文母語 C1 學習者的資源分享，2026-07 評估）：
  - 動詞變位每日小練習（la-conjugaison.fr、《Conjugaison progressive du français》débutant）→ 對應 2026-10「現在式核心動詞」milestone
  - 慢速法語 YouTube（Français avec Pierre、Easy French、innerFrench）→ 每天一支＋shadowing
  - Audiobook shadowing（《Le Petit Prince》，每天一段）→ A2 之後
  - Tandem 語伴 → 口說輸出，配合課堂糾音

### 換檔後的再評估條件

當自學進度領先課堂**超過一個單元**（預估 2026-11 ~ 12 發生）→ 評估把每週六團課換成或加上 italki 一對一（照自己進度走）。團課屆時的殘餘價值是口說團體練習，去留看當時感受。

課程進度記錄在各 lesson 筆記的「下週課程」區塊與 dashboard 的 Recent Lessons。

## 多教材整合：A1 固定複習章節

使用者手上有多份內容重疊的教材（法語協會課堂教材、Busuu、多鄰果、Assimil）。為避免同一主題在不同 App 各自零散重複，收斂成一份固定的章節複習順序，見 [a1-review-curriculum.md](a1-review-curriculum.md)：

- **主線＝法語協會課堂進度**：章節順序與內容深度以老師實際教過的（見 `01_lessons/`）為準，這也是唯一課堂驗證過、可正式收錄進 Knowledge Base 的內容
- **Busuu／多鄰果／Assimil＝補充，可以偷跑**：課堂還沒教到的章節（例如動詞變化）可以先用這三個 App 接觸混眼熟，但標記「待課堂驗證」，不算正式收錄，等課堂教到、對過老師版本後才移除標記
- 這條「補充教材可偷跑」規則只適用於**非音素內容**（單字、文法、句型、日期數字類）；Phase 1 期間的**音素**教學順序仍照上方「時期一：跟課期」的「不搶先自學」規則，兩者範疇不同、不衝突

## Milestones（2026-07 估算）

| 時間 | Milestone |
|---|---|
| 2026-08 中 | Phase 1 完成：音素聽辨穩定（minimal pairs >90%） |
| 2026-09 | IELTS 考完，換檔加大投入；能做完整自我介紹 |
| 2026-10 | 現在式核心動詞 + 數字/時間/日期 |
| 2026-11 | 日常情境撐 5–8 輪對話；評估 italki 一對一 |
| 2026-12 ~ 2027-01 | **考 A1**（TCF/TEF 或 DELF A1） |
| 2027 年底 | NCLC 7 目標（原定 2027 年中，依投入時數修正） |

## 老師（italki）策略

- **不要**一開始找一般 Conversation 老師（他們只改大錯，重點在聊得下去）
- 找專教 French pronunciation / phonetics / accent reduction 的老師
- 每週 1 次、30 分鐘即可，內容就是逐音確認：/y/ /u/ /ø/ /œ/、鼻母音、/ʁ/

## 對系統其他部分的影響

- `start today`：任務要對齊目前階段（Phase 1 期間以音素/minimal pairs/聽辨為主，不排大量單字任務）
- `收錄單字`：單字卡的 IPA 欄位是必填重點；Phase 3 起收錄時同時記錄「自己猜的 IPA vs 正確 IPA」的差異，作為錯誤證據來源
- Audio 練習（shadowing / chant）：優先服務當前階段正在練的音素或規則
