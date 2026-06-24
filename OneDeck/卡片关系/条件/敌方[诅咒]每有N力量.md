# 敌方[诅咒]每有N力量



## 需要该条件的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "卡片库"

WHERE any(map(conditions, (c) => contains(c, "[[" + this.file.path + "|" + this.file.name + "]]")))

```



## 能满足该条件的收益



- [[卡片关系/收益/增强敌方[诅咒]N|增强敌方[诅咒]N]]

- [[卡片关系/收益/将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒]|将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒]]]

- [[卡片关系/收益/给予敌方N力量|给予敌方N力量]]








