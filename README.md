# 抽签转盘

在线使用：https://yirochi08-arch.github.io/lucky-wheel/

输入名单，按「开始」，半圆转盘抽出结果。单个 `index.html`，不依赖任何外部资源，名单和设置只存在自己的浏览器里。

## 前台

- 半圆转盘 + 底座 + 中心「开始」按钮；两种转法：**指针摆动**（转盘不动、指针来回摆）或 **转盘旋转**（指针不动、转盘转圈，带拨片）。
- 转动时：跑马灯追光、指针残影、当前扇区高亮、标题实时滚动经过的名字、拨片/滴答音效。
- 落定时：中奖扇区弹出描边、其余变淡、灯泡齐闪、名字放大落定、彩带。
- 五套主题：奶油、夜场、糖果、黑白、线稿。

## 设置（右上角）

- **名单**：转盘名字；一行一个；打乱顺序、去掉重复、按数字生成；按权重抽时显示各项概率。
- **抽法**：每次抽几个（一个一个转 / 转一次全出）；抽中后放回、移出转盘或置灰；概率人人相同、按权重（`名字 | 3`）或洗牌轮转；指针停在扇区随机位置或正中。结果用 `crypto.getRandomValues` 事先决定，转盘只负责演出来。
- **外观**：主题、转动方式、时长、圈数/摆动次数、四种停下方式；文字、跑马灯、彩带、音效、结果卡片开关。
- **记录**：全部抽签记录。

## 参考的开源项目

- [CrazyTim/spin-wheel](https://github.com/CrazyTim/spin-wheel)：带权重的扇区、可配置时长与缓动
- [buuing/lucky-canvas](https://github.com/buuing/lucky-canvas)：先加速后减速的大转盘节奏
- [kilee1230/wheel-of-names](https://github.com/kilee1230/wheel-of-names)：中奖后直接「移出名单」
- [alsatianco/spin-the-wheel](https://github.com/alsatianco/spin-the-wheel)：纯静态、本地保存、用 crypto 随机数选结果
