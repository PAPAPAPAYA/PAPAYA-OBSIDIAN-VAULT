---
related to:
  - "[[将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒]]]"
  - "[[当友方获得力量时]]"
  - "[[所有卡上每有一力量]]"
  - "[[消耗所有友方N力量]]"
  - "[[造成N伤害]]"
  - "[[给予友方N力量]]"
---
# 力量倍化N



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(payoffs, (p) => contains(string(p), this.file.name)))

```



## 该收益可满足的条件



- [[所有卡上每有一力量|所有卡上每有一力量]]









