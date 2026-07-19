# Phase 1 練習指南 — 音素聽辨怎麼練、用什麼工具

> 這是 Phase 1（征服所有法語音）的具體操作手冊。策略層見 [learning_strategy.md](learning_strategy.md)，本週範圍見 [dashboard.md](dashboard.md)。

## 每日 20 分鐘的固定流程

```
① 純聽辨（8 分鐘）：聽目標 minimal pair，判斷「是哪個音」，不看拼字、不管意思
② 模仿錄音（8 分鐘）：跟著念，手機錄音，回放跟原音比對
③ 自測（4 分鐘）：隨機播 10 題，答對 9 題以上 = 這組過關
```

自測（第 ③ 步）輪替三種形式，別只做聽辨選字：
1. 聽音選字（傳統聽辨）
2. **聽音寫 IPA**（放例字 → 寫出 /IPA/ → 對音素卡）
3. **看 IPA 念出來**（看 /pɛ̃/ 念 pain → 錄音對 Forvo）

後兩種對應 [learning_strategy](learning_strategy.md) 的量化標準（發音→IPA >90%、IPA 辨識 >95%），每次自測至少含 3 題 IPA 雙向題。

過關的音組隔 2–3 天回測一次；一直分不出的音告訴 AI coach，記入 evidence log 追蹤。

## 課後 5 分鐘解碼（每次上完課 / 遇到新單字）

拿老師板書教過的字（或任何新字）5–10 個，走「預測→驗證→修正」五步。**必須先猜再對答案**，順序顛倒就沒有診斷價值：

```
① 拆：不查不聽，把拼字切段，每段對應一張音素卡
   例：restaurant → r | e+st | au | r | an | t
② 猜：靠卡片拼法表寫下自己猜的 IPA → /ʁɛstoʁɑ̃/
③ 對：查正確 IPA + 聽 Forvo 真人發音
④ 記：猜錯的段落歸因——
   - 規則沒記熟 → 回對應音素卡複習，錯的例字抄進卡
   - 卡片沒收這條拼法 → 拼法表補一行
   - 不規則字（femme /fam/）→ 進 vocabulary 條目個案記
   - 同類錯第 2、3 次 → 照 confidence policy 進 evidence log / error_db
⑤ 念：跟讀真人音 2–3 次收尾（猜對 ≠ 念得出來）
```

音素卡全套 34 張在 [pronunciation/phonemes/](../10_knowledge_base/pronunciation/phonemes/)，入口見 [voyelles-francaises](../10_knowledge_base/pronunciation/voyelles-francaises.md)、[consonnes-francaises](../10_knowledge_base/pronunciation/consonnes-francaises.md)。

## 工具（依用途）

### ① Interactive IPA Chart — 聽單音、建立音的分類
- 網址：ipachart.com（或搜 "interactive IPA chart"）
- 用法：點 /u/ 聽、點 /y/ 聽，來回切換聽差別，直到不用想就分得出
- 適合：每天流程的第 ① 步暖身

### ② Forvo — 聽真實單字的母語者發音
- 網址：forvo.com，搜尋單字就有多位母語者錄音
- 用法：搜 minimal pair 的兩個字輪流聽（tout / tu、vous / vu、peu / peur）
- 適合：第 ① 步主體 + 第 ② 步的模仿範本

### ③ YouTube — minimal pairs 訓練影片 + 嘴型示範
- 搜尋關鍵字：`French minimal pairs`、`French vowel discrimination`、`French phoneme training`、`French u ou pronunciation`
- 很多影片就是「tout / tu、tout / tu」輪播然後叫你猜，正是聽辨訓練
- 學不會的音（例如 /y/、/ʁ/）搜嘴型示範：`French u sound mouth position`——看舌位嘴型比純聽更快
- 推薦頻道：**Comme une Française**（發音練習，真人示範清楚）、**FrenchPod101**（發音專題，如 "Top 5 French pronunciation mistakes"）
- 適合：第 ①② 步都可用

### ③b 《Les 500 exercices de phonétique》A1/A2（Hachette FLE）— 系統化音素練習【已購入 2026-07-16】
- 紙本練習冊 + CD 音檔 + corrigés（解答），逐音攻克，比隨機影片更有結構
- CD 音檔已存在 `00_resources/500-exercices-phonetique-cd/`（461 個 mp3，已加入 .gitignore 不進版控）
- 來源：一位中文母語學習者（一年到 C1）分享她開頭一個月就用這本做密集發音練習，路線與 Phase 1 相同
- 用法：每天挑 1–2 個練習，取代或補充第 ①③ 步的素材。書上聽辨題＋corrigés 正好當第 ③ 步的自測題（有標準答案可對）
- **讀的順序不照書的頁碼**，見下方「500 exercices 讀序規劃」

### ④ 手機錄音 App（內建即可）— 自我比對
- 錄自己念 → 回放 → 跟 Forvo 原音對照
- 同一個錯誤連續出現時，把錄音留著，上課問老師或回報 AI coach

### ⑤ 線上課程《從0開始學法文｜路易教你旅遊日常會話》— 音素講解影片
- 已購買（目前進度 4%，停在 1-1）
- **Phase 1 只看第 1 章**：1-1 字母、1-2 母音類型（對應本週範圍）、1-3 特殊子音（下週六課堂範圍，可預習）、1-5 聯頌現象；1-4 陰陽性、1-6 順著看即可
- 價值：換一位老師示範同一批音素，幫助抓穩定特徵
- 第 2 章以後（情境會話、單字量）**留到 2026-09 換檔期**再排，見 learning_strategy

### ⑥ 之後才用，現在不用
- TV5MONDE（分級聽力）：等 A1 程度再開始
- Podcast Français Facile（結構化免費課程，含發音練習）：Phase 2 起可用
- Busuu（綜合會話 App，10–15 分鐘小單元）：Phase 1 不用（主體是單字＋情境會話，與發音優先衝突）。換檔期若想加碎片時間管道再評估，先跟路易課程比較避免重複；注意來源推薦（Zoe）含業配成分
- Anki：等 Phase 2 累積拼字規則後批次匯出；**不用**現成的「5000 高頻字」牌組——與「自己收錄＋IPA 預測驗證」路線衝突

## 《500 exercices de phonétique》讀序規劃（2026-07-16 排定）

書的編排是「節奏語調 → 母音 → 子音」，那是課堂教學順序；自學依 Phase 1 策略（先練穩單音、跟著課堂進度走），**調整為以下順序**：

### 第 1 批 — 母音（本週起，對應 Lesson 01 已教範圍）

| 順序 | 單元 | 頁碼 | 對應 |
|---|---|---|---|
| 1 | Partie II-2 [i]–[y]–[u] | p.36 | 已練過的 [u]/[y]，用書回測鞏固 |
| 2 | Partie II-3 [e]–[ɛ] | p.45 | **[i]/[e] 聽辨弱點**（evidence log 7/13），優先做 |
| 3 | Partie II-3 [ø]–[œ]、[o]–[ɔ] | p.51、57 | 週二音組回測 |
| 4 | Partie II-3 /E/–/Œ/–/O/ 綜合 | p.63 | 中母音總複習，當自測用 |
| 5 | Partie II-5 鼻母音（4 個小單元） | p.77–94 | 週三音組；最後的 [ɛ̃]–[ɑ̃]–[ɔ̃] 三分（p.94）當自測 |
| 6 | Partie II-1 [a] 和 [wa] | p.30 | [a] 與中文「啊」近似，快速帶過 |

### 第 2 批 — 子音（7/18 上完課後，跟老師教的進度走）

| 順序 | 單元 | 頁碼 | 備註 |
|---|---|---|---|
| 7 | Partie III-1 occlusives | p.102–130 | 中文母語者重點組：**[p]–[b]**（p.102）、**[b]–[v]**（p.108）——中文無濁塞音對立 |
| 8 | Partie III-2 constrictives | p.136–158 | 重點組：**[s]–[z]**（p.142）、**[ʃ]–[ʒ]**（p.148） |
| 9 | Partie III-3 liquides | p.162–174 | **/ʁ/**（p.162）+ **[ʁ]–[l]** 對比（p.174），Phase 1 的大魔王 |

### 第 3 批 — 韻律與 e muet（Phase 1 收尾，約 8 月上旬）

| 順序 | 單元 | 頁碼 | 對應 |
|---|---|---|---|
| 10 | Partie II-4 [ə] instable | p.69 | e muet 在 Phase 1 範圍 |
| 11 | Partie I：Rythme、Intonation、Liaisons | p.14、18、23 | liaison 在 Phase 1 範圍；單音穩了再練韻律才有效 |
| 12 | Introduction-1 Alphabets graphique et phonétique | p.7 | Lesson 01 已教過，快速核對 IPA 表即可 |

### 留給之後（不要現在讀）

- **Annexes「Phonie-graphie : voyelles / consonnes」（p.181–182）→ 這就是 Phase 2 的教材骨架**（拼字→發音規則），Phase 2 開始時從這裡起步，每條規則收進 `10_knowledge_base/pronunciation/`
- Annexes「Le « h » français」（p.183）→ Phase 2 一起讀
- Introduction-2 Chiffres et nombres（p.8）→ 對應 2026-10「數字/時間/日期」milestone
- Annexes「Les marques du français familier」（p.180）→ A2 之後

### 書的單元 ↔ 音素卡對照表

書是「成對練」、卡是「單音一張」，一個單元對應 2–3 張卡；卡上也都標了頁碼，雙向可查。檔名用拼法（phoneme-eu-ferme）不用 IPA，卡片 frontmatter 第一行是書上的符號。

| 書的單元（頁碼） | 對應音素卡 |
|---|---|
| [a] et [wa]（30） | phoneme-a、phoneme-w |
| [i]–[y]–[u]（36） | phoneme-i、phoneme-u（/y/）、phoneme-ou（/u/） |
| [e]–[ɛ]（45） | phoneme-e-ferme、phoneme-e-ouvert |
| [ø]–[œ]（51） | phoneme-eu-ferme、phoneme-eu-ouvert |
| [o]–[ɔ]（57） | phoneme-o-ferme、phoneme-o-ouvert |
| /E/–/Œ/–/O/（63） | 中母音六卡綜合自測，不對應單卡 |
| [ə]（69） | phoneme-e-muet |
| 鼻母音（77/83/88/94） | phoneme-in、phoneme-an、phoneme-on |
| [p]–[b]（102）/[b]–[v]（108）/[p]–[f]（113） | phoneme-p、-b、-v、-f |
| [t]–[d]（118）/[k]–[g]（124） | phoneme-t、-d、-k、-g |
| [m]–[n]–[ɲ]（130） | phoneme-m、-n、-gn |
| [f]–[v]（136）/[s]–[z]（142）/[ʃ]–[ʒ]（148）/[ʒ]–[j]（154）/綜合（158） | phoneme-f、-v、-s、-z、-ch（/ʃ/）、-j（/ʒ/）、-yod |
| [ʁ]（162）/[l]（168）/[ʁ]–[l]（174） | phoneme-r、phoneme-l |
| （書無單元） | phoneme-ui（/ɥ/）——靠 huit、je suis 自然練 |

## 本週（7/19–7/25）排程

> 每天三塊，各自獨立、互不取代：**①20 分鐘音素聽辨**（耳朵，跟單字量無關）、**②5 分鐘課後解碼**（老師教過的字，猜 IPA→對→念，材料取自 [decks/vocabulaire/](../08_ai/anki/decks/vocabulaire/)）、**③其他**（作業/Anki 複測/聽寫）。
> 上週 7/14–7/17 的項目無完成紀錄，母音部分（500 exercices 第 1 批）併入本週前兩天補做；後半週接 Lesson 02 的子音與數字。作業 cahier p.5 練習 1–3 + p.6 練習 1 拆在週二～週四完成，避免週五趕工。

| 日期 | ① 聽辨（20 分） | ② 課後解碼（5 分，猜→對→念） | ③ 其他 |
|---|---|---|---|
| 週日 7/19 | 補 [i] vs [e]（evidence log 7/13 弱點）：500 ex p.45；順帶回測 [u]/[y] | [temps-et-jours.md](../08_ai/anki/decks/vocabulaire/temps-et-jours.md) 8 字（jour/semaine/mois/demain…）| — |
| 週一 7/20 | 鼻母音三分 [ɛ̃]/[ɑ̃]/[ɔ̃]：500 ex p.77–94；搭配數字 0–20 聽辨 | [nombres.md](../08_ai/anki/decks/vocabulaire/nombres.md) 10 字 | — |
| 週二 7/21 | 子音 [p]–[b]、[b]–[v]：500 ex p.102、p.108；例字 bébé/pépé、hibou/poule | [personnes.md](../08_ai/anki/decks/vocabulaire/personnes.md) 5 字 | cahier p.5 練習 1 |
| 週三 7/22 | 子音 [s]–[z]、[ʃ]–[ʒ]：500 ex p.142、p.148；例字 poisson/poison、chat/ça、jupe/gîte | [animaux.md](../08_ai/anki/decks/vocabulaire/animaux.md) 7 字 | cahier p.5 練習 2 |
| 週四 7/23 | 數字 17–31 聽寫自測；liaison 跟讀 un euro/deux euros/un abricot；c/g 拼字規則自測 | [objets.md](../08_ai/anki/decks/vocabulaire/objets.md) 9 字 | cahier p.5 練習 3 + p.6 練習 1 |
| 週五 7/24 | 總自測：500 ex p.63 母音綜合 + p.94 鼻母音綜合 | [ecole-classe.md](../08_ai/anki/decks/vocabulaire/ecole-classe.md) 5 字 + [decks/phrases/](../08_ai/anki/decks/phrases/) 挑 5 句 | **Anki 卡庫全測一輪**（70 張，vocab+phrases）；見 [lesson-02 複習清單](../01_lessons/2026-07-18_lesson-02.md) |
| 週六 7/25 | 上課 | — | 課堂驗證；交作業（p.5×3 + p.6×1）|

自測（① 的第 ③ 小步）記得輪替聽音選字／聽音寫 IPA／看 IPA 念出來三種形式，見上方「每日 20 分鐘的固定流程」。

音素對應表見 [voyelles-francaises](../10_knowledge_base/pronunciation/voyelles-francaises.md)。

## 發音要領備忘

- **/y/**（tu）：先發 /i/ 的舌位，嘴唇縮圓；**/u/**（tout）舌頭更後
- **/ø/**（deux）：老師糾音重點「舌頭往後」
- 鼻母音：氣從鼻子出，嘴巴不收尾（不要念成 -n 結尾）

---
*建立：2026-07-12。每週日由 AI coach 依最新 lesson 更新「本週聽辨排程」。*
