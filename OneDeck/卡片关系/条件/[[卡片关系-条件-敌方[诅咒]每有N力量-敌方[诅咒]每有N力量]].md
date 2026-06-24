# [[卡片关系/条件/敌方[诅咒]每有N力量|敌方[诅咒]每有N力量]]



## 需要该条件的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "卡片库"

WHERE any(map(conditions, (c) => contains(c, "[[" + this.file.path + "|" + this.file.name + "]]")))

```



## 能满足该条件的收益



（暂无）






