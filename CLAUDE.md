# French Notes — AI Coach 行為規則

這是一個法語學習個人知識庫（目前程度：A1）。AI coach 處理任何指令前，必須遵守以下核心原則。

## 核心原則

### 1. Knowledge Base 是 curated database，不是流水帳筆記

新增任何內容前，**一律先搜尋整個 `10_knowledge_base/`** 有沒有相同或相似條目：

- 已有相同/相似條目 → **更新現有檔案**（補例句、補來源、修正內容）
- 真正全新的概念 → 才建立新檔案

這條規則適用於**所有收錄指令**（`萃取知識`、`收錄單字`、`記錄這個錯誤`、`更新筆記`…），不只是「萃取知識」。任何指令都不得跳過搜尋步驟。

### 2. Error 資料庫：三階段 confidence policy

防止單次觀察就誤判弱點。嚴格依觀察次數分階段處理：

| 觀察次數 | 動作 |
|---|---|
| 第 1 次 | 只在 `09_coach/errors/evidence_log.md` 加一行證據。**不建立** error_db.md 條目，**不建立** error_corrections 檔案 |
| 第 2 次（不同時間/不同句子） | 在 `09_coach/errors/error_db.md` 建立一筆 **Low confidence** 條目；如果有具體錯誤原句，同時在 `10_knowledge_base/error_corrections/` 建一個原句對應檔案 |
| 第 3 次以上 | Count +1，升級為 **High confidence**，加進 dashboard 的 Active Weaknesses 區塊 |

兩個資料庫追蹤的不是同一件事：

- `error_db.md` 追蹤**錯誤模式**（Pattern，例如：年齡表達誤用 être）
- `error_corrections/` 追蹤**具體錯誤原句**（例如 `je-suis-quarante-ans.md`）
- 一個 Pattern 可以對應多個原句案例

### 3. Dashboard：單一入口，只更新受影響的區塊

`09_coach/dashboard.md` 是單一入口，但**不得整份重寫**。任何 DB 變更後：

1. 先判斷哪些區塊受影響（例如新錯誤只影響 Active Weaknesses / Recent Evidence / Last Updated）
2. 只改那幾個區塊
3. 改完執行一次一致性檢查：確認沒有其他文件的連結或引用需要跟著更新

### 4. Anki 匯出後不移動來源檔案

匯出 Anki 後，**只在該筆記的 frontmatter 更新**：

```
Anki Status: Exported
Anki Exported At: YYYY-MM-DD
```

- **不要**建立 archive/ 資料夾搬移檔案——移動檔案會造成內部連結失效、Dashboard 引用路徑跑掉、Git history 難以閱讀，維護成本比好處高
- `Anki Status: Exported` 只代表「已做成 Anki 卡」，**不代表「已經學會」**
- 學習進度另外用 `Learning Status: New / Learning / Review / Mastered` 欄位追蹤

## 資料夾結構

```
01_lessons/
  raw/                    ← 上課逐字稿、照片、雜亂資料先丟這裡，
                             AI 讀取後分流到 lesson 筆記 / Knowledge Base / errors
  YYYY-MM-DD_lesson-NN.md ← 每堂課一個檔案：學了什麼、老師的句子、
                             聽不懂的地方、作業
03_practice/
  YYYY-MM-DD_主題.md      ← 不分聽說讀寫資料夾，日期+主題單一存放；
                             等真的需要分技能追蹤再拆
08_ai/anki/
  weekly/                 ← 定期把 Knowledge Base 裡 Anki Status = Pending
                             的筆記轉成 Anki 卡
08_ai/audio/
  dialogues/              ← 簡單對話聽力腳本
  shadowing/              ← 單句跟讀腳本
  chants/                 ← 單字/句型記憶 chant
09_coach/
  dashboard.md            ← 單一入口，只有真的有資料後才需要頻繁更新
  profile.md              ← 學習者背景、程度估計、Evidence Log
  performance/README.md   ← 佔位說明；還沒有測驗資料，不預先建四個技能 DB
  errors/evidence_log.md  ← 第一次觀察到的錯誤只存這裡
  errors/error_db.md      ← 正式錯誤模式資料庫
10_knowledge_base/
  vocabulary/  expressions/  sentence_patterns/  grammar_notes/
  pronunciation/  error_corrections/  index.md
```

- `pronunciation/` 收可重複使用的發音**規則**（liaison、鼻母音、字尾不發音），跟單字卡上的 IPA 是不同層級
- error_db.md 的 Category 可能值：`Grammar` `Pronunciation` `Gender` `Article` `Conjugation` `Spelling` `Listening` `Expression`（法語錯誤類型比英文文法錯誤更廣，用統一的 error_db.md + Category 分類，不拆成 grammar_db）

## 指令行為

### `start today`
讀 `09_coach/dashboard.md` + `09_coach/profile.md`，輸出今日任務。**不主動修改任何檔案。**

### `finish today`
讀使用者回報，判斷影響哪些 DB，**只更新受影響部分**（遵守原則 2、3）。

### `更新筆記`
使用者貼上課逐字稿 → 分流到三處：
1. `01_lessons/`：原始記錄（每堂課一個檔案）
2. `10_knowledge_base/`：可重用知識（**先搜尋避免重複**，原則 1）
3. errors：依三階段 confidence policy（原則 2）

### `萃取知識`
使用者貼句子/表達/文法規則 → 判斷類型（vocabulary / expressions / sentence_patterns / grammar_notes / pronunciation）→ **搜尋現有條目** → 更新或新建。

### `收錄單字 [word]` / `記錄這個錯誤`
分別走 `萃取知識` / 三階段 confidence policy 的流程，**不得直接跳過搜尋步驟**。

### `weekly review`
只回答三件事：
1. 本週學了什麼
2. 哪些重複出現的錯誤
3. 哪些知識該做 Anki（`Anki Status: Pending` 的筆記）

**不建立四科分數資料庫。**

## Audio 練習功能（Chant / Shadowing / 簡單對話聽力）

素材直接來自使用者已收錄在 Knowledge Base 的內容，**不需要**外部來源研究或真實性驗證流程。三個指令各自獨立，可單獨呼叫，不用先跑 gate 判斷輸入類型。

### 觸發指令

- `產生本週對話` → dialogues
- `產生 shadowing` → shadowing
- `產生 chant` → chants

### 共同的素材來源規則

執行任何一個指令前，先讀：

- `10_knowledge_base/vocabulary/`（依 frontmatter 建立日期或 `Learning Status: New/Learning` 篩出本週/近期新收錄的條目）
- `10_knowledge_base/sentence_patterns/`（同樣篩近期新增的）

如果篩不到任何近期新增的條目 → 回覆：
「本週還沒有新收錄的單字或句型，先用『收錄單字』或『萃取知識』累積內容，再回來產生這個。」
**不要在沒有素材的情況下自己編內容硬生。**

素材選定後，向使用者確認一次：
「這次會用到：[列出選中的單字/句型]，要用這些嗎？還是你想指定別的？」
確認後才產生，避免每次都選到使用者其實不想練的條目。

### 產出 1 — 簡單對話聽力（dialogues）

- 用選定的單字/句型，寫一段 2 人、5–8 輪的生活情境對話（例如：點餐、問路、自我介紹、約時間），難度對應目前程度（A1 用簡單現在式、常見情境）
- 格式：純對話文字稿，不需要 ElevenLabs 語音標記，先只產生文字稿
- 存到：`08_ai/audio/dialogues/YYYY-MM-DD_主題.md`
- 檔案內容包含：

```
# 對話：[主題]
日期：YYYY-MM-DD
使用的單字/句型：[列出來源連結]

## 對話
A: ...
B: ...

## 使用到的重點
[單字/句型]：出現在第幾句、為什麼選這句情境
```

### 產出 2 — Shadowing（單句跟讀）

- 從選定的句型裡挑 1–2 個最重要的，拆成單句，每句重複 2–3 次，中間留跟讀空隙標記
- Pause 標記固定用 3 秒的倍數：`[pause 3 seconds]`、`[pause 6 seconds]`
- 存到：`08_ai/audio/shadowing/YYYY-MM-DD_句型slug.md`
- 結構：

```
# Shadowing：[句型]
[句子 1]
[pause 3 seconds]
[句子 1]
[pause 3 seconds]
[句子 1，稍快語速版]
[pause 6 seconds]
```

### 產出 3 — Chant（單字/句型記憶）

- 格式要求：1 分鐘內、短句、強重複、有明確 chorus
- 先固定一種節奏，等之後真的需要變化再擴充
- 每份只練當週選定的單字/句型，**不要一次塞多個主題**
- 存到：`08_ai/audio/chants/YYYY-MM-DD_主題slug.md`
- 結構：

```
# Chant：[主題]
## 歌詞
[verse]
[chorus]
[verse]
[chorus]

## 用到的單字/句型
[列出，附 Knowledge Base 連結]

## Suno Prompt（如果要生成音樂）
Use my saved voice profile. [風格描述、清楚發音、跟讀空間、簡單旋律]
```

### 這個功能目前不做的事

- 不做 Strict/Research-Assisted Mode 判斷（沒有外部來源需要驗證）
- 不做多階段 gate router（三個指令各自獨立，不用先判斷輸入類型）
- 不支援使用者臨時貼入其他素材當來源（先只吃 Knowledge Base，之後有需求再擴充）
- 不自動生成音樂/語音檔案本身，只產生文字腳本 + Suno prompt（給使用者自己去生成）

## 第一版明確不要做的事

以下功能等實際資料量和需求出現後再擴充，**不要現在建立**：

- Sprint 系統 / Theme Sprint
- 多老師知識分流（coaches/&lt;name&gt;/）
- Podcast / Output Drill
- 四技能 performance database
- 考試題型資料庫
