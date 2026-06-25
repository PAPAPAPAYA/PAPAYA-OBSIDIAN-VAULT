# 力量倍化N



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(payoffs, (p) => contains(string(p), this.file.name)))

```



## 该收益可满足的条件



- [[卡片关系/条件/所有卡上每有一力量|所有卡上每有一力量]]









