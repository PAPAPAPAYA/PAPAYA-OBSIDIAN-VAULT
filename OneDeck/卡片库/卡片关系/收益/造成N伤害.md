---
related to:
  - "[[力量倍化N]]"
  - "[[当敌人受到伤害时]]"
  - "[[给予友方N力量]]"
  - "[[给予自身N力量]]"
  - "[[重复M次]]"
---
# 造成N伤害

## 拥有该收益的卡片

```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(payoffs, (p) => contains(string(p), this.file.name)))

```




