1.21.11以下版本未进行测试,请谨慎下载
## ✨ 功能特点
- **智能连锁挖矿**：自动挖掘相邻的同类矿物方块
- **右键切换**：手持镐子右键点击即可开启/关闭连锁挖矿
- **视觉反馈**：屏幕下方弹出式消息，清晰显示状态变化
- **音效反馈**：不同状态有不同音效提示
- **可配置性**：支持自定义连锁规则和行为
- **工具适配**：支持所有镐子类型，包括铜镐
- **矿物限制**：每种镐子仅能连锁挖掘其默认可挖掘的矿物
- **Folia 兼容**：完全适配 Folia 服务器
## 📋 兼容性
- **Paper**：1.21.11+  
- **Folia**：1.21.11+  
- **Java**：21+
## 📦 安装方法
1. 下载最新版本的 `ChainOre-1.0.0.jar`
2. 将 jar 文件放入服务器的 `plugins` 文件夹
3. 重启服务器
4. 插件自动生成配置文件
## 🎮 使用说明
### 基础操作
1. **手持任意镐子**
2. **右键点击**空气或方块
3. **查看反馈**：屏幕下方会显示连锁挖矿的开启/关闭状态
4. **开始挖矿**：在连锁挖矿开启状态下，挖掘矿物时会自动连锁挖掘相邻的同类矿物
### 连锁规则
- 连锁范围：仅挖掘当前方块周围的同类矿物方块
- 最大数量：可在配置文件中设置单次连锁的最大方块数
- 工具耐久：可选择是否根据连锁挖掘的方块数量消耗工具耐久
- 掉落处理：可选择直接放入背包或使用原版掉落规则
## ⚙️ 配置说明
插件生成两个配置文件：`config.yml` 和 `tool.yml`，位于 `plugins/ChainOre/` 目录下。
### config.yml - 主配置文件
```yaml
# ChainOre 主配置文件
# 单次连锁挖掘的最大方块数量限制
maxBlocksPerChain: 64
# 是否根据连锁挖掘的方块数量消耗工具耐久度
damageToolPerBlock: true
# 物品获取方式：true为直接放入背包，false为原版掉落规则
directToInventory: true
# 是否需要按住Shift键才能触发连锁挖掘
requireShift: false
# 允许使用连锁挖矿的世界列表（留空表示所有世界）
enabledWorlds: []
```
### tool.yml - 工具配置文件
配置每种镐子可连锁挖掘的矿物方块：
```yaml
# ChainOre 工具配置文件
# 配置每种镐子可连锁挖掘的矿物方块
#木镐
WOODEN_PICKAXE:
  - COAL_ORE
  - DEEPSLATE_COAL_ORE
  - GLOWSTONE
#石镐
STONE_PICKAXE:
  - COAL_ORE
  - DEEPSLATE_COAL_ORE
  - IRON_ORE
  - DEEPSLATE_IRON_ORE
  - COPPER_ORE
  - DEEPSLATE_COPPER_ORE
  - LAPIS_ORE
  - DEEPSLATE_LAPIS_ORE
  - REDSTONE_ORE
  - DEEPSLATE_REDSTONE_ORE
  - GLOWSTONE
  - NETHER_GOLD_ORE
  - NETHER_QUARTZ_ORE
# 其他镐子配置...
```
## 🔧 权限说明
| 权限节点 | 描述 | 默认值 |
|---------|------|-------|
| `chainore.mine` | 允许使用连锁挖矿功能 | `true` (所有玩家) |
| `chainore.admin` | 允许使用管理员命令 | `op` |
## 📝 命令说明
| 命令 | 描述 | 权限 |
|------|------|------|
| `/chainore reload` | 重载配置文件 | `chainore.admin` |
| `/chainore status` | 查看连锁挖矿状态 | `chainore.mine` |
## ❓ 常见问题
### 问题：连锁挖矿没有生效
- **检查**：是否手持镐子
- **检查**：是否右键开启了连锁挖矿
- **检查**：挖掘的矿物是否在当前镐子的可连锁列表中
- **检查**：是否在允许使用连锁挖矿的世界中
### 问题：连锁挖矿太消耗工具耐久
- **解决**：可以在 `config.yml` 中设置 `damageToolPerBlock: false`
### 问题：掉落物没有直接进入背包
- **解决**：可以在 `config.yml` 中设置 `directToInventory: true`
## 📖 更新日志
### v1.0.0 (2026-03-04)
- ✅ 初始版本发布
- ✅ 支持 Paper 1.21.11+ 和 Folia 1.21.11+
- ✅ 实现连锁挖矿核心功能
- ✅ 支持右键切换连锁状态
- ✅ 弹出式消息提示
- ✅ 可配置的连锁规则
- ✅ 支持所有镐子类型
- ✅ 适配铜镐
- ✅ 支持下界残骸、下界金矿石、下界石英矿石等
## 🤝 贡献
欢迎提交 Issue 和 Pull Request 来改进插件！
## 📄 开源协议
本插件采用 [MIT License](LICENSE) 开源
## 📧 联系方式
- **作者**：xpy
- **GitHub**：https://github.com/xpy/ChainOre
- **反馈**：欢迎在 GitHub 上提交 Issue
## 🎯 未来计划
- [ ] 添加更多配置选项
- [ ] 支持自定义连锁范围形状
- [ ] 添加粒子效果
- [ ] 支持更多工具类型
- [ ] 优化性能，支持更大规模的连锁挖掘
## 📌 注意事项
1. 请确保使用兼容版本的服务器软件
2. 首次安装后请检查配置文件
3. 定期备份配置文件
4. 如遇问题，请查看服务器日志
---
**ChainOre** - 让挖矿更高效，让游戏更有趣！ 🎮✨
[CODE]插件试用服务器:2a2t.org[/CODE]
