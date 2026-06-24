# [[卡片关系/收益/埋葬N友方[亡语]-[萦绕]|埋葬N友方[亡语]/[萦绕]]]



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "卡片库"

WHERE any(map(payoffs, (p) => contains(p, "[[" + this.file.path + "|" + this.file.name + "]]")))

```



## 该收益可满足的条件



（暂无）






