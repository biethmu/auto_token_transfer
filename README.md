# 自动发送本地代币工具

这是一个用于批量发送以太坊或其他 EVM 兼容链上的本地代币（例如 ETH、BNB、MATIC 等）的自动化工具。该脚本支持批量生成随机接收地址，并在用户账户余额充足的情况下自动完成转账。

---

## 功能特点
- **支持多种 EVM 兼容链**：通过用户提供的 RPC URL 连接链上网络。
- **批量转账**：用户可指定交易次数，每次生成随机接收地址并完成转账。
- **余额提示**：交易完成后显示账户剩余余额。
- **自动重试**：在遇到网络或交易失败时，支持多次重试。

---

## 环境要求
- Python 3.8 或更高版本
- 以太坊或其他 EVM 兼容链的 RPC 节点（如 Infura、Alchemy 或自建节点）

---

## 安装与运行

### 1. 克隆项目
首先克隆仓库到本地：
```bash
git clone https://github.com/ziqing888/auto_token_transfer.git
cd auto_token_transfer
```
### 2. 安装依赖
确保你的环境中安装了 pip，然后运行以下命令安装所需库：
```
pip install -r requirements.txt
```
### 3. 配置并运行脚本
运行脚本时会要求输入以下信息：

RPC URL：EVM 网络的节点地址（如 Infura、Alchemy 或其他 RPC 提供商提供的 URL）。
私钥：发送账户的私钥，建议仅用于测试或临时账户。
交易次数：需要发送的交易数量。
单次交易金额：每笔交易发送的代币数量。
### 运行脚本：
```
python3 bot.py
```
### 注意事项

请妥善保管您的私钥，避免在生产环境中直接使用主账户私钥。
RPC 节点性能：

建议使用可靠的 RPC 提供商以确保交易顺利完成。
