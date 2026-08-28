# 高速 ACT 战斗系统原型 · 逻辑层

UE 5.8 / 纯蓝图 / 个人项目 / 2026.08 至今

本仓库只包含本人自行编写的战斗逻辑与数据层，不包含任何第三方素材。完整设计说明见 [战斗设计案.pdf](战斗设计案.pdf)（16 页），演示视频与交互说明见 [winnnnk.github.io](https://winnnnk.github.io/)。

## 目录里有什么

| 路径 | 内容 |
| --- | --- |
| `Content/Combat_A/Blueprints/` | 玩家角色、玩家控制器、Boss、训练木桩、判定 Notify State、伤害接口 |
| `Content/Combat_A/Data/` | 帧数据表、反馈分级表、Boss 帧表、决系统调参资产，以及 5 个枚举与 2 个结构体 |
| `Content/Combat_A/Anim/` | 10 个 Animation Montage（Section、判定窗口与 Notify 全部手工放置） |
| `Content/Combat_A/Input/` | Enhanced Input 资产 |
| `Content/Combat_A/Maps/` | 白模竞技场关卡 |
| `Config/` | 工程配置 |

核心内容是 `Data/DT_AttackFrameData`：全部时序参数集中在这一张 23 列的数据表里，取消矩阵是它的视图、本身不存数值。

## 不包含什么，以及为什么

**动作资源包**。玩家动作来自付费购买的 9CG Sword Animation Pack，Boss 动作来自同作者的长矛包。授权允许在成品中使用，不允许以源资产形式再分发，因此不在本仓库中。

**Epic 提供的第三方内容**。ParagonRampage 与 Mannequins 等资产体积约 3.4 GB，且非本人作品，一并排除。

## 打开之后会看到什么

用 UE 5.8 打开 `.uproject`，蓝图图表、数据表、枚举与结构体均可正常查看和编辑。

由于缺少上述动作资源，10 个 Montage 会出现引用丢失，关卡无法正常运行。**本仓库的用途是查看逻辑与数据，不是运行 demo**；实际运行效果请看演示视频。

## 当前进度

玩家侧完整垂直切片已完成：输入缓冲与优先级仲裁、11 状态 × 3 输入取消矩阵、招式执行、球体扫描判定与单次挥砍去重、「决」资源的积累与分档释放、帧表运行时校验。

Boss 一阶段规格已完成定义，为下一里程碑。反馈链目前只实现了顿帧。

## 联系

吴云柯（Wink）· 15858252358@163.com
