# Xianyu Copywriter Skill

闲鱼文案生成技能 - 为OpenClaw AI助手提供专业的闲鱼商品文案生成能力。

## 功能特点

- ✅ **虚拟商品文案** - 软件、教程、模板、数字内容等专业文案
- ✅ **实物商品文案** - 二手商品、闲置物品等实物描述
- ✅ **文案优化** - 基于现有文案进行结构化优化
- ✅ **风险控制** - 降低售后纠纷的风险提示
- ✅ **关键词生成** - 提升搜索曝光的SEO优化

## 适用场景

- 想要"帮写闲鱼文案"
- 想要"生成闲鱼商品描述"
- 想要"优化这个闲鱼文案"
- 任何闲鱼商品描述相关的需求

## 安装方法

### 方法1：通过技能文件安装（推荐）

1. 下载 `.skill` 文件：
   ```bash
   # 下载技能包到OpenClaw工作目录
   wget https://github.com/[your-username]/xianyu-copywriter/raw/main/xianyu-copywriter.skill
   ```

2. 解压到OpenClaw技能目录：
   ```bash
   # 解压到OpenClaw技能目录
   unzip xianyu-copywriter.skill -d ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
   ```

3. 重启OpenClaw Gateway：
   ```bash
   openclaw gateway restart
   ```

### 方法2：通过源码安装

1. 克隆或下载源码：
   ```bash
   cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
   git clone https://github.com/[your-username]/xianyu-copywriter.git
   ```

2. 确保目录结构正确：
   ```
   openclaw/skills/
   └── xianyu-copywriter/
       ├── SKILL.md
       └── references/
           ├── virtual-product-template.md
           └── physical-product-template.md
   ```

3. 重启OpenClaw Gateway：
   ```bash
   openclaw gateway restart
   ```

### 方法3：手动复制（适用于本地开发）

1. 复制整个技能文件夹到OpenClaw技能目录

2. 重启OpenClaw Gateway

## 使用方法

### 直接对话触发

安装成功后，直接与OpenClaw对话即可触发技能：

```
帮写一个闲鱼文案，卖Python编程教程
```

```
生成一个95新的AirPods Pro的闲鱼商品描述
```

```
优化这个闲鱼文案：[粘贴你的文案]
```

### 提供详细信息

为了生成更好的文案，可以提供以下信息：

- **商品类型**：虚拟商品 / 实物商品
- **产品名称**：核心产品名称
- **核心卖点**：3-5个主要特点
- **目标用户**：适合人群/限制条件
- **售价范围**（可选）
- **特殊说明**：版权、授权、售后政策等

## 文案示例

### 虚拟商品示例

**请求：** "帮我写一个闲鱼文案，卖Seedance 2.0视频提示词服务"

**输出：** 包含警告说明、购买须知、产品介绍、版权声明、关键词等完整模块

### 实物商品示例

**请求：** "生成一个95新的AirPods Pro的闲鱼文案"

**输出：** 包含产品详情、外观状态、功能测试、交易保障、发货信息等完整模块

## 文件说明

```
xianyu-copywriter/
├── SKILL.md                              # 技能主文件（AI读取使用）
├── README.md                             # 安装说明（这个文件）
├── references/
│   ├── virtual-product-template.md       # 虚拟商品文案模板
│   └── physical-product-template.md      # 实物商品文案模板
└── xianyu-copywriter.skill               # 技能包文件（用于分发）
```

## 技能结构

- **SKILL.md**: 技能核心文件，包含技能描述、工作流程、最佳实践
- **references/**: 参考文档目录
  - virtual-product-template.md: 虚拟商品标准模板，支持软件、教程、模板等
  - physical-product-template.md: 实物商品标准模板，支持二手商品、闲置物品等

## 核心能力

### 虚拟商品文案生成

- ⚠️ 开头重点警告（年龄限制、技术要求、无退款声明）
- 💰 购买须知（虚拟商品属性、版权禁止条款）
- 📦 产品介绍（编号分段的详细描述）
- 🔒 版权声明（禁止二传二改、二次盈利）
- 🏷️ 关键词标签（提升搜索曝光）

### 实物商品文案生成

- 🎯 产品亮点（核心卖点）
- 📦 产品详情（规格参数、使用情况）
- ✅ 交易保障（正品保证、发货时效）
- ⚠️ 注意事项（售后政策）

### 文案优化

- 添加明确的风险提示
- 优化排版（使用emoji分隔）
- 补充版权声明
- 生成关键词标签

## 技巧和最佳实践

### 文案风格

- 简洁明了，直击要点
- 风险前置，虚拟商品开头即说明限制
- 结构清晰，使用emoji和编号分段
- 诚实透明，不夸大不隐瞒

### 降低纠纷技巧

1. **明确告知** - 虚拟商品强调"无法退款"
2. **技术门槛** - 说明使用难度
3. **版权保护** - 明确禁止二传二改
4. **预期管理** - 说明产品能力边界

### 排版规范

使用emoji增强可读性：
- ⚠️ 警告/注意事项
- 💰 价格/退款政策
- 📦 产品介绍
- 🔒 版权声明
- ✅ 交易保障
- 🏷️ 关键词标签

## 兼容性

- **OpenClaw版本**: v22.22.0+
- **支持平台**: 所有OpenClaw支持的通信平台（Feishu、微信、Telegram等）
- **模型要求**: 任何支持中文的AI模型

## 开发

### 技能开发指南

参考OpenClaw官方技能开发文档：
https://docs.openclaw.ai/skills

### 贡献

欢迎提交Issue和Pull Request来优化这个技能！

## 许可证

MIT License

## 联系方式

- GitHub Issues: https://github.com/[your-username]/xianyu-copywriter/issues
- 作者: OpenClaw Community

## 更新日志

### v1.0.0 (2026-02-16)
- ✅ 初始版本发布
- ✅ 支持虚拟商品文案生成
- ✅ 支持实物商品文案生成
- ✅ 支持文案优化
- ✅ 完整的模板和参考文档

---

**Made with ❤️ for OpenClaw**
