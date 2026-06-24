# 生成[诅咒]N



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "卡片库"

WHERE any(map(payoffs, (p) => contains(p, "[[" + this.file.path + "|" + this.file.name + "]]")))

```



## 该收益可满足的条件



- [[卡片关系/条件/再有N敌人被揭晓|再有N敌人被揭晓]]

- [[卡片关系/条件/当敌方[诅咒]揭晓时|当敌方[诅咒]揭晓时]]

- [[卡片关系/条件/所有卡上每有一力量|所有卡上每有一力量]]








