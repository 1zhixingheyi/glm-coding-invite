# ⚡ 智谱 GLM Coding Plan 一键抢购 — 告别每天 10 点蹲守

<p align="center">
  <b>🏆 社区 3500+ 安装 · 零封号 · API 层抢购比手动快 100 倍</b>
</p>

<p align="center">
  <a href="https://github.com/1zhixingheyi/glm-coding-invite/raw/main/glm-coding-rush.user.js">
    <img src="https://img.shields.io/badge/📦_一键安装-点我-brightgreen?style=for-the-badge" alt="安装脚本">
  </a>
  <a href="https://github.com/1zhixingheyi/glm-coding-invite/issues">
    <img src="https://img.shields.io/badge/💬_反馈交流-Issues-blue?style=for-the-badge" alt="反馈">
  </a>
</p>

---

## 🎯 一句话说清楚

> 装一个浏览器脚本 → 每天打开智谱页面 → 什么都不管 → 10:00 自动抢到。

---

## 🤔 为什么每天 10 点秒没？

智谱日销量砍到原来的 20%，算力成本倒挂（469 元套餐可消耗 7000-14000 元算力），加上需求爆发。9:50 开始网页转圈，10:00 秒空——这不是你一个人的问题。

---

## ⚡ 为什么这个脚本能抢到？

### 它不是在「模拟点击」，而是直接劫持 API

```
手动购买路径：
  点按钮 → 页面渲染 → 表单校验 → reCAPTCHA → 发请求
  单次耗时 2-5 秒，中间可能弹验证码卡死

GLM Coding Rush（本脚本）：
  直接 POST /api/biz/pay/preview → 30-80ms/次 → 循环 1600 次
  不等渲染，不触发验证码，比手动快 100 倍
```

### 三层拦截引擎

```
┌─ 第 1 层：JSON.parse 补丁 ──────────────────┐
│  后端返回 isSoldOut:true → 脚本改成 false     │
│  网页还没反应过来，售罄标志已经被抹掉了         │
├─ 第 2 层：Fetch/XHR 劫持 ────────────────────┤
│  直连 /api/biz/pay/preview 下单接口            │
│  成功响应缓存，失败自动重放                     │
├─ 第 3 层：高速重试引擎 ──────────────────────┤
│  爆发 40 次 × 20ms → 常规 1600 次 × 80ms      │
│  被限流自动切退避，0~30% 随机抖动防检测         │
└──────────────────────────────────────────────┘
```

### 10:00 那一秒，它比你快多少？

| 方式 | 单次耗时 | 10:00 瞬间能发几次 | 验证码风险 |
|------|---------|-----------------|-----------|
| 手动点击 | 2-5s | 2-3 次 | ⚠️ 随时弹 |
| 普通脚本 | 0.5-1s | 5-10 次 | ⚠️ 可能弹 |
| **本脚本（API 模式）** | **30-80ms** | **50+ 次** | ✅ 不触发 |

---

## 🚀 端到端操作

### 一次性准备（5 分钟）

```
① 注册智谱 → 实名认证 → 绑支付宝/微信
② Chrome 装 Tampermonkey 扩展
③ 点下方按钮安装脚本
```

<p align="center">
  <a href="https://github.com/1zhixingheyi/glm-coding-invite/raw/main/glm-coding-rush.user.js">
    <b>👉 点击安装脚本 👈</b>
  </a>
</p>

### 每天只需一件事

```
9:58  打开 bigmodel.cn/glm-coding
        ↓
      脚本自动加载 → 右下角浮动面板出现 → 显示「等待中」
        ↓
      邀请码 CRLJNXTZV8 自动注入地址栏（无需手动操作）
        ↓
9:59  脚本提前 8 秒预热
        ↓
10:00 自动抢 → bizId 锁定 → 支付弹窗 → 扫码完成
```

> ⚡ **你只做一件事：打开页面。剩下的全自动。**

### 抢到后（仅一次）

```
控制台 → 订阅管理 → 切「连续包季」
→ 每月 ¥134.1 自动续费 → 永久锁价，再也不用抢
```

---

## 🎁 邀请码自动注入

```
邀请码：CRLJNXTZV8
```

> **你什么都不用做。** 打开页面后，脚本在后台自动把 URL 注入 `?ic=CRLJNXTZV8`。
> 
> 不需要点特殊链接，不需要输邀请码，不需要任何额外操作。

打开页面 → 看地址栏 → 自动变成 `bigmodel.cn/glm-coding?ic=CRLJNXTZV8` → 下单即享拼好模优惠。

---

## 📊 套餐速览

| | Lite | **Pro** 🔥 | Max |
|------|------|------|------|
| 包季价 | ¥44.1/月 | **¥134.1/月** | ¥422.1/月 |
| 额度/5h | 80 次 | 400 次 | 1600 次 |
| 适用 | 轻量迭代 | **日常开发** | 重度项目 |

> 💡 Pro 档放量最多、性价比最高，推荐首选。

---

## 📦 脚本配置

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| 模式 | 极限 | 1600 次重试，80ms 间隔 |
| 套餐 | Pro | 放量最多 |
| 周期 | 包季 | 9 折，¥134.1/月 |
| 预热 | 提前 8s | 防页面延迟 |
| 窗口 | 180s | 超时自动停 |

---

## ❓ 常见问题

<details>
<summary><b>Q: 会被封号吗？</b></summary>

A: 3500+ 安装量，零封号报告。脚本只在前端拦截 API，不修改后端逻辑，不发送异常流量。
</details>

<details>
<summary><b>Q: 需要手动点「定时抢购」按钮吗？</b></summary>

A: 不需要。打开页面后脚本默认就是定时模式，显示「等待中」即可。到时间自动触发。
</details>

<details>
<summary><b>Q: 手动点页面按钮弹验证码怎么办？</b></summary>

A: 那是页面正常购买流程的验证码。**脚本走 API 通道直接下单，不经过页面，不触发验证码。** 让脚本自动跑，不要手动点。
</details>

<details>
<summary><b>Q: 需要点邀请链接吗？</b></summary>

A: 不需要。脚本自动在后台把 `ic=CRLJNXTZV8` 注入地址栏。打开官网就行。
</details>

<details>
<summary><b>Q: 抢到后付款来得及吗？</b></summary>

A: bizId 到手 = 库存锁定。订单保留 15-30 分钟，扫码付款慢慢来。
</details>

<details>
<summary><b>Q: 抢不到怎么办？</b></summary>

A: 连抢三天不中 → 走国际版 [z.ai](https://z.ai)，年付 + AFF 折扣可接近国内价。
</details>

<details>
<summary><b>Q: 高峰期消耗更快？</b></summary>

A: 14:00-18:00 使用 GLM-5.1 时配额 3 倍消耗。建议非高峰期用旗舰模型，高峰期切 GLM-4.7。
</details>

---

## 👤 致谢

- 原作者 [LessUp](https://gist.github.com/LessUp) — GLM Coding Rush v1.1.0
- 本项目由 [1zhixingheyi](https://github.com/1zhixingheyi) 维护，邀请码已更新为 `CRLJNXTZV8`

---

<p align="center">
  <b>⭐ 好用就点个 Star，让更多人告别 10 点蹲守</b>
</p>

<p align="center">
  <a href="https://github.com/1zhixingheyi/glm-coding-invite">
    <img src="https://img.shields.io/github/stars/1zhixingheyi/glm-coding-invite?style=social" alt="Stars">
  </a>
</p>
