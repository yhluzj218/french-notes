# French Notes

法語學習個人知識庫，供 AI coach 使用。目前程度：A1。

## 結構

- [01_lessons/](01_lessons/) — 課堂記錄；雜亂原始資料先丟 `raw/`，由 AI 分流
- [03_practice/](03_practice/) — 練習記錄（日期+主題，不分技能）
- [08_ai/anki/](08_ai/anki/) — Anki 匯出（`weekly/` 放每期匯出檔）
- [09_coach/](09_coach/) — AI coach 的工作區：dashboard、profile、錯誤資料庫
- [10_knowledge_base/](10_knowledge_base/) — curated 知識庫（單字/表達/句型/文法/發音/錯誤原句）

## 常用指令

| 指令 | 作用 |
|---|---|
| `start today` | 讀 dashboard + profile，輸出今日任務 |
| `finish today` | 依回報更新受影響的 DB |
| `更新筆記` | 貼逐字稿，分流到 lessons / knowledge base / errors |
| `萃取知識` | 貼句子/規則，搜尋後更新或新建條目 |
| `收錄單字 [word]` | 收錄單字（先搜尋避免重複） |
| `記錄這個錯誤` | 依三階段 confidence policy 記錄 |
| `weekly review` | 週回顧：學了什麼、重複錯誤、該做的 Anki |

行為規則詳見 [CLAUDE.md](CLAUDE.md)。
