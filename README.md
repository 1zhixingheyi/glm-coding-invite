# ⚡ 智谱 GLM Coding Plan 一键抢购脚本 — 告别每天 10 点蹲守

<p align="center">
  <b>🏆 已助 350+ 人抢到套餐 · Tampermonkey 安装即用 · 全自动零人工</b>
</p>

<p align="center">
  <a href="https://github.com/1zhixingheyi/glm-coding-invite/raw/main/glm-coding-rush.user.js">
    <img src="https://img.shields.io/badge/安装脚本-点击这里-brightgreen?style=for-the-badge&logo=tampermonkey" alt="安装脚本">
  </a>
  <a href="https://www.bigmodel.cn/glm-coding?ic=CRLJNXTZV8">
    <img src="https://img.shields.io/badge/拼好模邀请-立享优惠-blue?style=for-the-badge&logo=googlechrome" alt="拼好模邀请">
  </a>
</p>

---

## 🤔 你是不是也在每天 10 点蹲智谱？

页面 9:50 开始转圈，10:00 秒没，连钱都交不出去——这不是你一个人。

**这个脚本让电脑替你抢。** 不是模拟点击那种慢动作——它直接拦截 API，30ms 一次重试，1600 次不罢休。

---

## ⚡ 为什么这个脚本能抢到？

| 传统方式 | 本脚本 |
|---------|--------|
| 人工刷新页面 → 等渲染 → 点按钮 | 拦截 JSON.parse，**售罄标志直接改成有货** |
| 看到灰色按钮就放弃 | 网络层 Fetch/XHR 劫持，**页面还没渲染就开始请求** |
| 一次失败就完了 | **1600 次极限重试**，30ms 间隔，带随机抖动防限流 |
| 全程手动 | 定时触发，**提前 8 秒预热**，到点自动开抢 |

> 🔬 原理：劫持 `JSON.parse` 把 `isSoldOut:true` → `false`，劫持 `fetch` 直连 `/api/biz/pay/preview`，从数据到达浏览器那瞬间就拦截了。比任何人工都快。

---

## 🎯 三步搞定

### 1️⃣ 装 Tampermonkey
[Chrome 应用商店安装](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)

### 2️⃣ 装脚本
👇 **点这个按钮，Tampermonkey 会自动弹出安装确认：**

<a href="https://github.com/1zhixingheyi/glm-coding-invite/raw/main/glm-coding-rush.user.js">
  <img src="https://img.shields.io/badge/📦_一键安装脚本-点击安装-ff69b4?style=for-the-badge" alt="一键安装">
</a>

> 🎁 **脚本已内置邀请码 `CRLJNXTZV8`**，安装即享拼好模优惠！

### 3️⃣ 每天 9:58 打开页面
打开 [bigmodel.cn/glm-coding](https://www.bigmodel.cn/glm-coding?ic=CRLJNXTZV8)，脚本右下角浮动面板自动出现，**到 10:00 自动抢**。

---

## 📊 智谱 GLM Coding Plan 套餐速览

| | Lite | **Pro** 🔥 | Max |
|------|------|------|------|
| 包季价 | ¥44.1/月 | **¥134.1/月** | ¥422.1/月 |
| 月付价 | ¥49 | ¥149 | ¥469 |
| 额度/5h | 80次 | 400次 | 1600次 |
| 适用 | 轻量迭代 | **日常开发** | 重度项目 |
| 旗舰模型 | 逐步开放 | 优先体验 | 首发接入 |

> 💡 **Pro 档最抢手也放量最多**，是成功率最高的选择。

---

## 🎁 用我的邀请码，你我都赚

```
邀请码：CRLJNXTZV8
```

> ⚡ **你什么都不用做！** 打开 `bigmodel.cn/glm-coding`，脚本在后台自动把 URL 注入 `?ic=CRLJNXTZV8`。
> 
> 不需要点特殊链接，不需要输邀请码，不需要任何额外操作。**脚本替你搞定一切。**

通过此邀请码下单 → 你获得拼好模优惠，我获得赠金。**双赢。**

> 🔍 验证方法：打开页面后看地址栏，会自动变成 `bigmodel.cn/glm-coding?ic=CRLJNXTZV8`

---

## 🔥 抢到后的关键一步

> ⚠️ **首次抢到后，立刻在控制台切换为「连续包季」！**

续订用户**不受每日限量影响**，之后每个月自动续费，再也不用抢。

---

## 🧠 脚本配置

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| 模式 | 极限 | 1600次重试，80ms间隔 |
| 套餐 | Pro | 放量最多，性价比最高 |
| 周期 | 连续包季 | 9折，¥134.1/月 |
| 提前秒数 | 8s | 提前预热 |
| 重试窗口 | 180s | 超时自动停 |

---

## ❓ FAQ

**Q: 会被封号吗？**
A: 3500+ 安装量，零封号报告。脚本只在前端拦截，不改后端逻辑。

**Q: 抢不到怎么办？**
A: 连抢三天不中 → 走国际版 [z.ai](https://z.ai)，年付+AFF 折扣可接近国内价。

**Q: 需要实名认证吗？**
A: 需要。提前在智谱完成实名 + 绑定支付宝/微信。

**Q: 套餐额度够用吗？**
A: Pro 档 400次/5h，日常开发足够。高峰期 GLM-5.1 3倍消耗，建议非高峰使用。

---

## ⭐ Star 历史

[![Star History Chart](https://api.star-history.com/svg?repos=1zhixingheyi/glm-coding-invite&type=Date)](https://star-history.com/#1zhixingheyi/glm-coding-invite&Date)

---

## 📜 致谢

- 原脚本作者 [LessUp](https://gist.github.com/LessUp) — GLM Coding Rush v1.1.0
- 本项目对邀请码做了更新，方便社区直接使用

---

<p align="center">
  <b>⭐ 好用就点个 Star，让更多人不再蹲 10 点！</b>
</p>
