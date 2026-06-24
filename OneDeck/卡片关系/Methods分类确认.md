# Methods 分类与收益→条件映射确认

> 已按你的确认更新：消耗力量/置顶力量最多敌方/埋葬后N卡均视为 condition；萦绕映射为「当卡片在墓地中」。

## 1. Method / Tag 分类表

| 原始 method / tag | 分类 | 归一化标签 |
| --- | --- | --- |
| `[tag]萦绕` (来自tag) | condition | 当卡片在墓地中 |
| `再有{N}<counter>敌人被揭晓` | condition | 再有N敌人被揭晓 |
| `减少{N}个敌方{N}力量` | payoff | 减少N个敌方N力量 |
| `力量倍化{N}` | payoff | 力量倍化N |
| `去除{N}[次元裂缝]` | payoff | 去除N[次元裂缝] |
| `友方被埋葬` | condition | 友方被埋葬 |
| `埋葬{N}友方` | payoff | 埋葬N友方 |
| `埋葬{N}友方[亡语]/[萦绕]` | payoff | 埋葬N友方[亡语]/[萦绕] |
| `埋葬{N}敌方` | payoff | 埋葬N敌方 |
| `埋葬后{N}卡` | condition | 埋葬后N卡 |
| `墓地每有{N}友方` | condition | 墓地每有N友方 |
| `增强敌方[诅咒]{N}` | payoff | 增强敌方[诅咒]N |
| `增强自身[诅咒]{N}` | payoff | 增强自身[诅咒]N |
| `将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒]` | payoff | 将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒] |
| `当卡被埋葬时` | condition | 当卡被埋葬时 |
| `当友方获得力量时` | condition | 当友方获得力量时 |
| `当友方被去除时` | condition | 当友方被去除时 |
| `当敌人受到伤害时` | condition | 当敌人受到伤害时 |
| `当敌方[诅咒]揭晓时` | condition | 当敌方[诅咒]揭晓时 |
| `当敌方[诅咒]获得力量时` | condition | 当敌方[诅咒]获得力量时 |
| `揭晓时` | condition | 揭晓时 |
| `敌方[诅咒]每有{N}力量` | condition | 敌方[诅咒]每有N力量 |
| `本回合每置顶过{N}友方` | condition | 本回合每置顶过N友方 |
| `每揭晓{N}<counter>次` | condition | 每揭晓N次 |
| `洗牌后` | condition | 洗牌后 |
| `消耗{N}力量` | condition | 消耗N力量 |
| `消耗敌方[诅咒]{N}力量` | condition | 消耗敌方[诅咒]N力量 |
| `添加自身到卡组中` | payoff | 添加自身到卡组中 |
| `生成[诅咒]{N}` | payoff | 生成[诅咒]N |
| `生成{N}[次元裂缝]` | payoff | 生成N[次元裂缝] |
| `给予下{X}卡{N}力量` | payoff | 给予下X卡N力量 |
| `给予友方{N}力量` | payoff | 给予友方N力量 |
| `给予敌方{N}力量` | payoff | 给予敌方N力量 |
| `置顶{N}友方` | payoff | 置顶N友方 |
| `置顶力量最多的敌方` | condition | 置顶力量最多的敌方 |
| `置顶敌方[诅咒]` | payoff | 置顶敌方[诅咒] |
| `置顶自身` | payoff | 置顶自身 |
| `获得力量时` | condition | 获得力量时 |
| `被埋葬` | condition | 被埋葬 |
| `被置顶` | condition | 被置顶 |
| `转移所有友方的{N}力量到自身` (拆分) | condition | 消耗所有友方N力量 |
| `转移所有友方的{N}力量到自身` (拆分) | payoff | 给予自身N力量 |
| `造成{N}伤害` | payoff | 造成N伤害 |
| `造成{N}伤害x{M}` (拆分) | condition | 重复M次 |
| `造成{N}伤害x{M}` (拆分) | payoff | 造成N伤害 |
| `造成{N}伤害x本回合被埋葬的敌方数量` (拆分) | condition | 本回合每有一敌方被埋葬 |
| `造成{N}伤害x本回合被埋葬的敌方数量` (拆分) | payoff | 造成N伤害 |
| `造成友方数量的伤害` (拆分) | condition | 每有一友方 |
| `造成友方数量的伤害` (拆分) | payoff | 造成N伤害 |
| `造成所有卡的力量数量的伤害` (拆分) | condition | 所有卡上每有一力量 |
| `造成所有卡的力量数量的伤害` (拆分) | payoff | 造成N伤害 |

## 2. 收益 → 条件 映射建议

| 收益 (payoff) | 能满足的条件 |
| --- | --- |
| 减少N个敌方N力量 | （暂无） |
| 力量倍化N | 所有卡上每有一力量 |
| 去除N[次元裂缝] | （暂无） |
| 埋葬N友方 | 友方被埋葬、墓地每有N友方、当卡片在墓地中、当卡被埋葬时、被埋葬 |
| 埋葬N友方[亡语]/[萦绕] | 友方被埋葬、墓地每有N友方、当卡片在墓地中、当卡被埋葬时、被埋葬 |
| 埋葬N敌方 | 当卡被埋葬时、本回合每有一敌方被埋葬 |
| 增强敌方[诅咒]N | 当敌方[诅咒]揭晓时、当敌方[诅咒]获得力量时、所有卡上每有一力量、敌方[诅咒]每有N力量、消耗敌方[诅咒]N力量、置顶力量最多的敌方 |
| 增强自身[诅咒]N | 当友方获得力量时、所有卡上每有一力量、消耗所有友方N力量 |
| 将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒] | 当敌方[诅咒]获得力量时、敌方[诅咒]每有N力量、消耗敌方[诅咒]N力量、置顶力量最多的敌方 |
| 添加自身到卡组中 | 每有一友方 |
| 生成N[次元裂缝] | 当友方被去除时、揭晓时、本回合每置顶过N友方、每揭晓N次、每有一友方、被置顶 |
| 生成[诅咒]N | 再有N敌人被揭晓、当敌方[诅咒]揭晓时、所有卡上每有一力量 |
| 给予下X卡N力量 | 当友方获得力量时、所有卡上每有一力量、消耗N力量、消耗所有友方N力量、获得力量时、重复M次 |
| 给予友方N力量 | 当友方获得力量时、所有卡上每有一力量、消耗N力量、消耗所有友方N力量、获得力量时、重复M次 |
| 给予敌方N力量 | 当敌方[诅咒]获得力量时、所有卡上每有一力量、敌方[诅咒]每有N力量、消耗敌方[诅咒]N力量 |
| 给予自身N力量 | 当友方获得力量时 |
| 置顶N友方 | 揭晓时、本回合每置顶过N友方、每揭晓N次、被置顶 |
| 置顶敌方[诅咒] | （暂无） |
| 置顶自身 | 揭晓时、本回合每置顶过N友方、每揭晓N次、被置顶 |
| 造成N伤害 | 当敌人受到伤害时 |

## 3. 每张卡片的 Conditions / Payoffs 预览

### 高等传送门 (`ADVANCE_PORTAL`) — Uncommon
- **conditions**: 每揭晓N次
- **payoffs**: 置顶N友方

### 人人为我 (`ALL_FOR_ONE`) — Uncommon
- **conditions**: 揭晓时, 所有卡上每有一力量
- **payoffs**: 造成N伤害

### 全能人 (`ALMIGHTY`) — Rare
- **conditions**: 揭晓时
- **payoffs**: 造成N伤害, 置顶N友方, 埋葬N敌方, 给予友方N力量, 生成N[次元裂缝], 增强敌方[诅咒]N

### 对生物兵器 (`ANTI_CREATURE_WEAPON`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 埋葬N敌方

### 复仇者 (`AVENGER`) — Uncommon
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 造成N伤害, 给予友方N力量

### 铁匠 (`BLACKSMITH`) — Common
- **conditions**: 揭晓时
- **payoffs**: 造成N伤害, 给予友方N力量

### 盲眼战斗牧师 (`BLIND_COMBAT_PRIEST`) — Common
- **conditions**: 揭晓时
- **payoffs**: 给予下X卡N力量

### 人间大炮 (`BODY_CANON`) — Rare
- **conditions**: 揭晓时, 重复M次, 墓地每有N友方
- **payoffs**: 造成N伤害

### 碎骨聚集体 (`BONE_COMBINATION`) — Uncommon
- **conditions**: 揭晓时, 本回合每有一敌方被埋葬
- **payoffs**: 造成N伤害

### 推进器 (`BOOSTER`) — Rare
- **conditions**: 洗牌后, 揭晓时
- **payoffs**: 置顶N友方, 埋葬N友方

### 棺材制造者 (`COFFIN_MAKER`) — Common
- **conditions**: 揭晓时
- **payoffs**: 造成N伤害, 埋葬N敌方

### 错乱传送术士 (`CONFUSED_PORTALMANCER`) — Uncommon
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 埋葬N友方, 生成N[次元裂缝]

### 冥界大炮 (`CORPSE_CANON`) — Uncommon
- **conditions**: 揭晓时, 友方被埋葬
- **payoffs**: 埋葬N友方, 造成N伤害

### 乌合之众 (`CROW_CROWD`) — Rare
- **conditions**: 揭晓时
- **payoffs**: 将所有友方的力量(排除友方[诅咒])转移到敌方的[诅咒]

### 被诅咒的尸体 (`CURSED_CORPSE`) — Uncommon
- **conditions**: 揭晓时, 被埋葬, 重复M次
- **payoffs**: 增强敌方[诅咒]N, 造成N伤害

### 被诅咒的骷髅 (`CURSED_SKELETON`) — Uncommon
- **conditions**: 揭晓时, 墓地每有N友方
- **payoffs**: 增强敌方[诅咒]N

### 诅咒附魔 (`CURSE_ENCHANTMENT`) — Rare
- **conditions**: 当敌人受到伤害时, 当卡片在墓地中
- **payoffs**: 增强敌方[诅咒]N

### 咒食的召唤师 (`CURSE_SUMMONER`) — Common
- **conditions**: 揭晓时, 消耗敌方[诅咒]N力量
- **payoffs**: 置顶N友方

### 咒食的野兽 (`CURSE_THIRST_BEAST`) — Uncommon
- **conditions**: 当敌方[诅咒]揭晓时, 揭晓时
- **payoffs**: 置顶自身, 造成N伤害

### 咒食的萨满 (`CURSE_THIRST_SHAMAN`) — Uncommon
- **conditions**: 揭晓时, 敌方[诅咒]每有N力量
- **payoffs**: 给予友方N力量

### 咒食的召唤师 (`CURSE_THIRST_SUMMONER`) — Uncommon
- **conditions**: 揭晓时, 消耗敌方[诅咒]N力量
- **payoffs**: 置顶N友方, 给予下X卡N力量

### 临终诅咒 (`DEATHBED_CURSE`) — Rare
- **conditions**: 当友方被去除时, 当卡片在墓地中
- **payoffs**: 给予敌方N力量

### 恶化 (`DETERIORATION`) — Rare
- **conditions**: 揭晓时, 敌方[诅咒]每有N力量
- **payoffs**: 增强敌方[诅咒]N

### 曼哈顿博士 (`DR_MANHATTAN`) — Uncommon
- **conditions**: 揭晓时, 消耗N力量
- **payoffs**: 置顶N友方, 埋葬N敌方

### 远古魔法使用者 (`ELDER_SORCERER`) — Rare
- **conditions**: 揭晓时, 本回合每置顶过N友方
- **payoffs**: 给予友方N力量

### 不散的恶灵 (`ETERNAL_GHOST`) — Rare
- **conditions**: 当敌人受到伤害时, 当卡片在墓地中
- **payoffs**: 造成N伤害

### 坠入裂缝 (`FALL_INTO_RIFT`) — Common
- **conditions**: 揭晓时
- **payoffs**: 生成N[次元裂缝], 埋葬N敌方

### 血肉聚集体 (`FLESH_COMBINATION`) — Uncommon
- **conditions**: 揭晓时, 每有一友方
- **payoffs**: 造成N伤害

### 哥布林暗杀部队 (`GOBLIN_ASSASSIN_TEAM`) — Uncommon
- **conditions**: 揭晓时, 被置顶
- **payoffs**: 造成N伤害, 埋葬N敌方

### 哥布林冲锋部队 (`GOBLIN_CHARGE_TEAM`) — Uncommon
- **conditions**: 揭晓时, 被置顶
- **payoffs**: 造成N伤害

### 冥界邀请 (`GRAVE_INVITATION`) — Uncommon
- **conditions**: 揭晓时, 墓地每有N友方
- **payoffs**: 造成N伤害, 埋葬N敌方

### 守墓人 (`GRAVE_KEEPER`) — Rare
- **conditions**: 揭晓时, 当卡被埋葬时
- **payoffs**: 造成N伤害, 置顶自身

### 冥界裂缝 (`GRAVE_PORTAL`) — Common
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 埋葬N敌方, 置顶N友方

### 尸爆 (`GRAVE_PUNCH`) — Common
- **conditions**: 揭晓时, 重复M次
- **payoffs**: 埋葬N友方, 造成N伤害

### 同路人 (`GRAVE_TOGETHER`) — Common
- **conditions**: 揭晓时
- **payoffs**: 埋葬N友方, 埋葬N敌方

### 卡位增加 <中> (`IncreaseDeckSize`) — Uncommon
- **conditions**: （无条件）
- **payoffs**: （无收益）

### 卡位增加 <小> (`IncreaseDeckSizeLite`) — Common
- **conditions**: （无条件）
- **payoffs**: （无收益）

### 早睡早起 (`IncreaseHpMax`) — Uncommon
- **conditions**: （无条件）
- **payoffs**: （无收益）

### 大范围死亡 (`LARGE_SCALE_DEATH`) — Rare
- **conditions**: 揭晓时, 埋葬后N卡
- **payoffs**: （无收益）

### 疯狂科学家 (`MAD_SCIENTIST`) — Common
- **conditions**: 揭晓时
- **payoffs**: 给予下X卡N力量

### 殉道者 (`MARTYR`) — Rare
- **conditions**: 被埋葬
- **payoffs**: 给予友方N力量

### 飞蛾人 (`MOTH_MAN`) — Uncommon
- **conditions**: 当敌方[诅咒]获得力量时
- **payoffs**: 置顶N友方

### 咒师 (`POISONER`) — Common
- **conditions**: 揭晓时
- **payoffs**: 增强敌方[诅咒]N, 造成N伤害

### 力量渴求者 (`POWER_CRAVER`) — Uncommon
- **conditions**: 揭晓时, 获得力量时
- **payoffs**: 造成N伤害, 力量倍化N

### 力量虹吸人 (`POWER_SIPHONER`) — Rare
- **conditions**: 揭晓时, 消耗所有友方N力量, 重复M次
- **payoffs**: 给予自身N力量, 造成N伤害

### 能量迸发 (`POWER_SURGE`) — Uncommon
- **conditions**: 揭晓时, 被置顶
- **payoffs**: 造成N伤害, 给予友方N力量

### 力量转移 (`POWER_TRANSFER`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 减少N个敌方N力量, 给予友方N力量

### 拔苗助长 (`PREMATURE`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 置顶敌方[诅咒]

### 增殖的厄运 (`PROLIFERATING_CURSE`) — Rare
- **conditions**: 揭晓时
- **payoffs**: 生成[诅咒]N

### 快速响应协议 (`QUICK_RESPONSE_PROTOCOL`) — Uncommon
- **conditions**: 再有N敌人被揭晓, 当卡片在墓地中
- **payoffs**: 置顶N友方

### 次元棺材 (`RIFT_COFFIN`) — Uncommon
- **conditions**: 当友方被去除时, 当卡片在墓地中
- **payoffs**: 埋葬N敌方

### 异次元的诅咒 (`RIFT_CURSE`) — Common
- **conditions**: 揭晓时
- **payoffs**: 增强敌方[诅咒]N, 生成N[次元裂缝]

### 次元吞噬者 (`RIFT_DEVOURER`) — Rare
- **conditions**: 揭晓时, 当友方被去除时
- **payoffs**: 造成N伤害, 给予友方N力量

### 次元龙 (`RIFT_DRAGON`) — Uncommon
- **conditions**: 揭晓时, 被置顶
- **payoffs**: 生成N[次元裂缝], 造成N伤害

### 次元引导者 (`RIFT_GUIDE`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 去除N[次元裂缝], 埋葬N敌方

### 次元虫 (`RIFT_INSECT`) — Common
- **conditions**: 揭晓时
- **payoffs**: 造成N伤害, 生成N[次元裂缝]

### 次元兽 (`RIFT_MONSTER`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 去除N[次元裂缝], 造成N伤害

### 裂缝召唤师 (`RIFT_SUMMONER`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 去除N[次元裂缝], 置顶N友方

### 献祭仪式 (`SACRIFICE_RITUAL`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 埋葬N友方, 生成N[次元裂缝]

### 献祭诅咒 (`SACRIFICIAL_CURSE`) — Common
- **conditions**: 揭晓时
- **payoffs**: 埋葬N友方, 增强敌方[诅咒]N

### 献祭剑 (`SACRIFICIAL_SWORD`) — Common
- **conditions**: 揭晓时
- **payoffs**: 埋葬N友方, 给予友方N力量

### 替死鬼 (`SCAPEGOAT`) — Uncommon
- **conditions**: 被埋葬
- **payoffs**: 造成N伤害, 置顶N友方

### 有副作用的传送门 (`SIDE_EFFECT_PORTAL`) — Common
- **conditions**: 揭晓时
- **payoffs**: 增强自身[诅咒]N, 置顶N友方

### 史莱姆 (`SLIME`) — Rare
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 造成N伤害, 添加自身到卡组中

### 小范围死亡 (`SMALL_SCALE_DEATH`) — Uncommon
- **conditions**: 揭晓时, 埋葬后N卡
- **payoffs**: 增强敌方[诅咒]N

### 屠夫 (`SNATCHER`) — Uncommon
- **conditions**: 揭晓时, 被置顶, 被埋葬
- **payoffs**: 造成N伤害, 置顶N友方, 埋葬N敌方

### 骷髅士兵 (`SOLDIER_SKELETON`) — Common
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 造成N伤害, 置顶自身

### 针刺骷髅 (`SPIKE_SKELETON`) — Uncommon
- **conditions**: 揭晓时, 被埋葬, 重复M次
- **payoffs**: 造成N伤害, 造成N伤害

### 战术爆破手 (`TACTICAL_BREACHER`) — Uncommon
- **conditions**: 揭晓时, 被置顶
- **payoffs**: 造成N伤害, 给予友方N力量

### 愚者 (`THE_FOOL`) — Common
- **conditions**: 揭晓时, 置顶力量最多的敌方
- **payoffs**: 造成N伤害

### 不死诅咒者 (`UNDEAD_CURSER`) — Common
- **conditions**: 揭晓时, 被埋葬
- **payoffs**: 增强敌方[诅咒]N

### 未完成的机器人 (`UNFINISHED_ROBOT`) — Rare
- **conditions**: 揭晓时
- **payoffs**: 造成N伤害, 力量倍化N

### 不稳定传送门 (`UNSTABLE_PORTAL`) — Uncommon
- **conditions**: 揭晓时
- **payoffs**: 置顶N友方, 埋葬N友方

### 武器精灵 (`WEAPON_SPIRIT`) — Uncommon
- **conditions**: 当友方获得力量时, 当卡片在墓地中
- **payoffs**: 给予友方N力量

### 不愚蠢的埋葬 (`WISE_BURIAL`) — Rare
- **conditions**: 被置顶
- **payoffs**: 埋葬N友方[亡语]/[萦绕]


