# done/ — 已錄入 Anki 的卡片

使用者回報「這些卡已經錄進 Anki」後，AI coach 把對應卡片從 `decks/` 移到這裡：

- **單字卡**：從 `decks/vocabulaire/<類別>.md` 剪下該卡區塊，貼進本資料夾同名的 `<類別>.md`（沒有就建立）
- **句型卡**：整個 md 檔從 `decks/phrases/` 移過來

規則：
- 位置即狀態——`decks/` = 待錄入、`done/` = 已在 Anki 裡
- 卡片內容搬移時不修改（保留 IPA、註記原樣）
- KB 來源檔案（10_knowledge_base/）永遠不動，動的只有卡片檔
- 「已錄入 Anki」≠「已學會」——學習進度看 KB 條目的 Learning Status
