# 重复M次



## 需要该条件的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(conditions, (c) => contains(string(c), this.file.name)))

```



## 能满足该条件的收益



- [[卡片关系/收益/给予下X卡N力量|给予下X卡N力量]]

- [[卡片关系/收益/给予友方N力量|给予友方N力量]]









