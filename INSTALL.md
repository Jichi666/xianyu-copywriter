# OpenClaw闲鱼文案生成技能 - 安装教程

## 前置要求

本技能需要您已经部署了OpenClaw AI助手环境。如果还没有OpenClaw，请先安装OpenClaw。

---

## 安装方法一：从GitHub克隆（推荐）

### 步骤1：打开终端/命令行

### 步骤2：进入OpenClaw技能目录

```bash
cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
```

⚠️ **注意：** 如果您的OpenClaw安装路径不同，请根据实际情况调整路径。常见路径：
- `~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/`
- `/usr/local/lib/node_modules/openclaw/skills/`
- `$(npm root -g)/openclaw/skills/`

### 步骤3：克隆技能仓库

```bash
git clone https://github.com/Jichi666/xianyu-copywriter.git
```

### 步骤4：验证安装

```bash
cd xianyu-copywriter
ls -la
```

应该看到以下文件：
```
SKILL.md
README.md
INSTALL.md
references/
├── virtual-product-template.md
└── physical-product-template.md
```

### 步骤5：重启OpenClaw Gateway

```bash
openclaw gateway restart
```

### 步骤6：测试使用

在OpenClaw中发送消息测试：

```
帮我写一个闲鱼文案
```

如果AI能够正常生成闲鱼文案，说明安装成功！

---

## 安装方法二：手动下载安装

### 步骤1：下载源码包

访问GitHub仓库：https://github.com/Jichi666/xianyu-copywriter

点击绿色"Code"按钮，选择"Download ZIP"下载源码包

### 步骤2：解压文件

下载完成后解压ZIP文件

### 步骤3：复制到OpenClaw技能目录

将解压后的`xianyu-copywriter`文件夹整个复制到OpenClaw技能目录

```bash
# 如果使用命令行复制
cp -r xianyu-copywriter ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
```

或使用图形界面直接复制粘贴

### 步骤4：重启OpenClaw Gateway

```bash
openclaw gateway restart
```

---

## 安装方法三：技能包安装（如果提供.skill文件）

### 步骤1：下载.skill文件

⚠️ 注意：如果没有.skill文件，请使用方法一或方法二

### 步骤2：解压技能包

```bash
cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
unzip xianyu-copywriter.skill
```

### 步骤3：重启OpenClaw Gateway

```bash
openclaw gateway restart
```

---

## 常见问题

### Q1: 如何找到OpenClaw安装路径？

运行以下命令查找：

```bash
npm root -g
```

路径一般为 `[npm root目录]/openclaw/skills/`

常见的完整路径示例：
- `~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/`
- `/usr/local/lib/node_modules/openclaw/skills/`

### Q2: 重启OpenClaw后技能没有生效？

检查以下几点：

1. 文件结构是否正确
   ```bash
   cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/xianyu-copywriter
   ls -la SKILL.md
   ```
   必须有SKILL.md文件

2. OpenClaw版本是否兼容
   ```bash
   openclaw --version
   ```
   需要v22.22.0+版本

3. 查看OpenClaw日志
   ```bash
   openclaw logs
   ```

### Q3: 没有git命令怎么办？

如果没有git，使用**方法二**（手动下载安装），或者先安装git：

```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install git

# CentOS/RHEL
sudo yum install git

# macOS
brew install git

# Windows
# 从 git-scm.com 下载安装包
```

### Q4: 权限问题？

如果遇到权限错误，尝试：

```bash
# 使用sudo（需要管理员权限）
sudo git clone https://github.com/Jichi666/xianyu-copywriter.git

# 或修改目录权限
sudo chmod -R 755 ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
```

### Q5: 如何验证技能是否加载成功？

方法一：查看OpenClaw启动日志
```bash
openclaw logs
```
查找是否有`xianyu-copywriter`相关加载信息

方法二：直接测试
在OpenClaw对话页面发送：
```
帮我写闲鱼文案
```

---

## 卸载方法

如果需要卸载此技能：

```bash
cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/
rm -rf xianyu-copywriter
openclaw gateway restart
```

---

## 更新方法

```bash
cd ~/.nvm/versions/node/v22.22.0/lib/node_modules/openclaw/skills/xianyu-copywriter
git pull
openclaw gateway restart
```

---

## 使用示例

安装成功后，可以直接与OpenClaw对话：

### 示例1：生成虚拟商品文案

```
帮写一个闲鱼文案，卖Python编程视频教程，包含50节课，售价99元
```

### 示例2：生成实物商品文案

```
生成一个95新的AirPods Pro的闲鱼文案
```

### 示例3：优化现有文案

```
优化这个闲鱼文案：[粘贴你的文案]
```

### 示例4：生成关键词

```
为iPhone 15 Pro生成闲鱼搜索关键词
```

---

## 技术支持

遇到问题时：

1. 查看官方文档：https://docs.openclaw.ai
2. 查看OpenClaw日志：`openclaw logs`
3. 检查文件结构完整性
4. 确认OpenClaw版本兼容性

---

**祝使用愉快！**
