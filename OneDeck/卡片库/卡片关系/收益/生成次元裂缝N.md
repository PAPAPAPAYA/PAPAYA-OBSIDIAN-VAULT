---
related to:
  - "[[去除次元裂缝N]]"
  - "[[当友方被去除时]]"
  - "[[每有一友方]]"
  - "[[置顶N友方]]"
---
# 生成次元裂缝N



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(payoffs, (p) => contains(string(p), this.file.name)))

```



## 该收益可满足的条件


- [[当友方被去除时|当友方被去除时]]

- [[OneDeck/卡片库/卡片关系/条件/揭晓时|揭晓时]]

- [[本回合每置顶过N友方|本回合每置顶过N友方]]

- [[每揭晓N次|每揭晓N次]]

- [[每有一友方|每有一友方]]

- [[被置顶|被置顶]]
- 
- [[去除次元裂缝N|去除次元裂缝N]]









