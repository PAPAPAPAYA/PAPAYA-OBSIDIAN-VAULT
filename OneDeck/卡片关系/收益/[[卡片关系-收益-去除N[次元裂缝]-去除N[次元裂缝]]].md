# [[卡片关系/收益/去除N[次元裂缝]|去除N[次元裂缝]]]



## 拥有该收益的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "卡片库"

WHERE any(map(payoffs, (p) => contains(p, "[[" + this.file.path + "|" + this.file.name + "]]")))

```



## 该收益可满足的条件



（暂无）






