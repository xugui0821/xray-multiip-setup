# xray-multiip-setup

自动化生成X-UI多IP出口配置的工具

## 快速开始
```
bash <(wget -qO- -o- https://github.com/xugui0821/x-ui-multiip-setup/raw/main/start.sh)
```

配置完成后使用生成的端口创建添加入站即可使用对应IP出站。


## 功能特性

- 自动检测服务器公网IP地址
- 交互式设置起始端口号
- 生成完整的Xray多IP出口配置
- 自动备份并更新x-ui.db数据库
- 自动重启x-ui服务使配置生效
- 自动检测并安装sqlite3依赖
- ## 使用示例
```
🔍 检测到 2 个公网 IP:

1. 203.0.113.1
2. 203.0.113.2

📌 请输入起始端口 [默认: 10001]: 20000

🔄 正在生成配置文件...
✅ 配置已保存到: /path/to/config.json

🔧 正在更新数据库...
📦 数据库备份: /etc/x-ui/x-ui.db.bak.20230825
✅ 数据库更新成功

🔄 正在重启 X-UI 服务...
🎉 配置完成！端口绑定信息:
• 端口 20000 → 203.0.113.1
• 端口 20001 → 203.0.113.2
```

