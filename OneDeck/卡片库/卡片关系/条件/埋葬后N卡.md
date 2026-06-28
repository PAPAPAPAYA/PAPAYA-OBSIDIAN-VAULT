---
related to:
  - "[[友方被埋葬]]"
  - "[[当卡被埋葬时]]"
  - "[[本回合每有一敌方被埋葬]]"
  - "[[被埋葬]]"
---
# 埋葬后N卡



## 需要该条件的卡片



```dataview

TABLE displayName AS 卡片, rarity AS 稀有度

FROM "OneDeck/卡片库"

WHERE any(map(conditions, (c) => contains(string(c), this.file.name)))

```



## 能满足该条件的收益

- [[被埋葬]]
- [[友方被埋葬]]
- [[当卡被埋葬时]]
- [[本回合每有一敌方被埋葬]]









