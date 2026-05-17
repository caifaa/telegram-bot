# TG Shop Bot + Web Admin

独立通用版 Telegram 商品/充值机器人，奥特曼主题UI。

## 功能介绍
- 💎 Premium会员购买
- ✨ 星币购买
- 💰 余额充值（支持USDT/OKPay）
- 👨‍💼 代理管理（独立机器人和后台）
- 📱 网页后台（奥特曼主题）

## 安装
```bash
cd 24小时会员
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Linux
pip install -r requirements.txt
copy .env.example .env
```

修改 `.env` 里的 `BOT_TOKEN`、管理员账号、支付地址。

## 启动方式
### 同时运行机器人和后台（推荐）
```bash
python main.py
```
- 后台地址：http://服务器IP:8000
- 默认账号：`admin`
- 默认密码：`admin123`

## 后台功能
- 🏠 首页（数据概览）
- 📦 商品管理
- 👥 用户管理
- 📋 订单管理（确认充值、查看状态）
- 🔘 按钮配置
- 📢 广播消息
- 👨‍💼 代理管理（一键克隆机器人）

## 支付说明
支持两种支付方式：
- USDT：转账到指定地址，自动检测到账
- OKPay：创建支付链接，用户支付后自动加余额

## 代理功能
- 每个代理有独立的机器人和后台
- 代理可配置自己的收款地址和管理员ID
- 机器人启动时自动向管理员发送后台地址
