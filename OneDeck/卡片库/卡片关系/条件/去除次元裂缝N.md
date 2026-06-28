---
related to:
  - "[[当友方被去除时]]"
  - "[[生成次元裂缝N]]"
---
# 去除次元裂缝N

## 拥有该条件的卡片

```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(conditions, (p) => contains(string(p), this.file.name)))

```

## 该条件可满足的条件

- [[当友方被去除时]]

## 能满足该条件的收益

- [[生成次元裂缝N]]







