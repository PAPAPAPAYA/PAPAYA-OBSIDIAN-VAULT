---
related to:
  - "[[置顶N友方]]"
---
# 每揭晓N次



## 需要该条件的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(conditions, (c) => contains(string(c), this.file.name)))

```



## 能满足该条件的收益



- [[生成次元裂缝N|生成次元裂缝N]]

- [[置顶N友方|置顶N友方]]

- [[置顶自身|置顶自身]]









