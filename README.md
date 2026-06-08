# 🚀 智谱 GLM Coding Plan — 一键抢购脚本

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> 每天 10:00 限量抢购智谱编程套餐？这个 Tampermonkey 脚本帮你自动搞定。

## 📊 套餐价格（2026年6月）

| 套餐 | 包季价 | 月付价 | 额度/5h |
|------|--------|--------|---------|
| Lite | ¥44.1 | ¥49 | 80次 |
| **Pro** 🔥 | **¥134.1** | ¥149 | 400次 |
| Max | ¥422.1 | ¥469 | 1600次 |

> 💡 Pro 档性价比最高，推荐日常开发使用。

## 🎁 使用邀请码立享优惠

👉 **拼好模邀请链接**：https://www.bigmodel.cn/glm-coding?ic=CRLJNXTZV8

通过此链接订阅，你我都可获得最高 20% 赠金！

## ⚡ 一键安装

1. 安装 [Tampermonkey](https://www.tampermonkey.net/) 浏览器扩展
2. [点击安装脚本](https://github.com/1zhixingheyi/glm-coding-invite/raw/main/glm-coding-rush.user.js)
3. 每天 9:58 打开 [bigmodel.cn/glm-coding](https://bigmodel.cn/glm-coding?ic=CRLJNXTZV8)，脚本自动 10:00 抢购

## 🔧 脚本功能

- ✅ 自动解锁售罄按钮
- ✅ 高速重试引擎（1600次，30ms级）
- ✅ JSON.parse 补丁绕过 isSoldOut
- ✅ Fetch/XHR 拦截 + 缓存回放
- ✅ 支付弹窗自动保护
- ✅ 秒级定时触发（提前8秒预热）
- ✅ 可拖拽浮动面板

## 📖 抢购策略

| 模式 | 重试次数 | 间隔 | 适用 |
|------|---------|------|------|
| 极限 | 1600 | 80ms | 网络好 |
| 稳健 | 900 | 120ms | 网络一般 |

推荐配置：**极限模式 + Pro套餐 + 连续包季**

## ⚠️ 注意事项

- 需提前在智谱完成实名认证 + 绑定支付方式
- 高峰期 (14:00-18:00) GLM-5.1 3倍消耗
- 首次抢到后**立即切连续包季**，续订不受限量影响

## 📜 License

MIT — 原脚本作者 [LessUp](https://gist.github.com/LessUp)，邀请码已更新。

---

⭐ 如果对你有帮助，给个 Star！
