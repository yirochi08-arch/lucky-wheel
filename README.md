# 抽签转盘

在线使用：https://yirochi08-arch.github.io/lucky-wheel/

输入名单，点一下转盘，抽出结果。单个 `index.html`，不依赖任何外部资源，名单和设置只存在自己的浏览器里。

## 设置项

- **名单**：一行一个；可打乱顺序、去重、一键生成数字（如 1–30）。
- **抽签方式**：每次抽几个（一个一个转 / 转一次全出）；抽中后放回、移出转盘、或留着置灰。
- **随机方式**：人人等概率、按权重（名单里写 `名字 | 3`，扇区按权重变大）、洗牌轮转（一轮内每项都中一次才重新开始）；指针停在扇区内随机处或正中。结果用 `crypto.getRandomValues` 事先决定，转盘只负责演出来。
- **显示效果**：指针转 / 转盘转；线稿、单色、多彩三种样式；主色；转动时长与圈数；四种停下方式（平稳减速、慢慢挪到、冲过头再回弹、先加速再减速）；转盘文字、结果弹窗、彩带、音效开关；标题文字可改。

## 参考的开源项目

- [CrazyTim/spin-wheel](https://github.com/CrazyTim/spin-wheel)：带权重的扇区、可配置时长与缓动的 spinTo
- [buuing/lucky-canvas](https://github.com/buuing/lucky-canvas)：先加速后减速的大转盘节奏
- [kilee1230/wheel-of-names](https://github.com/kilee1230/wheel-of-names)：中奖弹窗里直接「移出名单」
- [alsatianco/spin-the-wheel](https://github.com/alsatianco/spin-the-wheel)：纯静态、本地保存、用 crypto 随机数选结果
