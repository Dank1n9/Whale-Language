# 鲸语（Whale-Language）

一只只属于你的鲸鱼同伴，有可能实现你的愿望，还可以陪你聊天。

**Minecraft Fabric 模组**，AI 对话基于 DeepSeek API（需要玩家自行申请 API Key）。

<a href="https://whale.shiorko.dpdns.org" style="display: inline-block; padding: 18px 40px; font-size: 28px; font-weight: bold; color: #fff; background-color: #4CAF50; border-radius: 12px; text-decoration: none; text-align: center;">
  点我获取模组
</a>

## 版本目录

| 目录 | Minecraft 版本 | 说明 |
|---|---|---|
| `鲸语-2.1.4-fabric-1.21.1` | 1.21.1 | Fabric |
| `鲸语-2.1.4-fabric-1.21.3` | 1.21.3 | Fabric |
| `鲸语-2.1.4-fabric-1.21.4` | 1.21.4 | Fabric |
| `鲸语-2.1.4-fabric-1.21.11` | 1.21.11 | Fabric |

每个目录都是标准结构：`src/main/java`（源码）+ `src/main/resources`（fabric.mod.json、图标、皮肤贴图）。

## 功能

- **召唤鲸鱼娘**：使用贝壳（海晶碎片合成）召唤
- **认主 / 取名 / 转让**：右键认主，改名界面，`/ds give <玩家名>` 转让
- **AI 对话**：`/ds <名字> <内容>` 或聊天框提到名字，接入 DeepSeek 生成台词
- **指令执行**：AI 答应给物品时自动执行 `give`（AI 判定是否真给）
- **9 套皮肤**：`/ds config` 换皮肤按钮循环切换
- **记忆系统**：按存档独立记忆，聊多了 AI 自动提炼重要记忆
- **物品栏**：蹲下右键打开原版箱子界面（前5格=主手+装备）
- **死亡保留**：死亡不掉落，特殊贝壳复活恢复全部物品栏
- **PVP 决斗**：`/ds <名字> pvp` 和鲸鱼娘打架（创造模式会提示换生存）
- **主动战斗**：鲸鱼娘会主动攻击敌对生物、血低逃跑、跟随主人
- **AI 指令**：`/ds clear` 清空记忆、`/ds config` 配置界面

## 使用前提

1. 需要 **Fabric Loader** 和 **Fabric API**
2. 在 `https://api.deepseek.com` 注册并申请 API Key
3. 游戏内 `/ds config` 填入 API Key 并开启 AI

## 编译说明

本项目使用手动编译流程（tiny-remapper + javac），未使用 Gradle：
1. 需要 yarn mappings（官方→intermediary→named）
2. 编译脚本与打包脚本在开发环境（`fabric/compile_fabric*.ps1`、`fabric/build_tamper.ps1`）
3. 各版本 API 差异较大（1.21.11 尤其：`getEntityWorld`、`LazyEntityReference`、`WriteView/ReadView` 等）

## 版权

© 2026 Shiorko. All rights reserved.
https://copyright.shiorko.dpdns.org/

特别感谢：relish./(///▽///)～
