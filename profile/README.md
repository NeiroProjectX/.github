<p align="center">
  <img src="https://raw.githubusercontent.com/NeiroProjectX/.github/main/neiro-banner.png" width="640" alt="Neiro">
</p>


<p align="center">
  <strong>为 iOS 而生的原生 ASMR 播放器</strong> 
</p>
<p align="center">
  沉浸 · 原生 · 本地
</p>
<p align="center">
  A native iOS ASMR player powered by ASMR.ONE — crafted for the moments before sleep.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Swift-FA7343?logo=swift&logoColor=white" alt="Swift">
  <img src="https://img.shields.io/badge/iOS-17.0%2B-000000?logo=apple&logoColor=white" alt="iOS 17+">
  <img src="https://img.shields.io/badge/SwiftUI-BE4041?logo=swift&logoColor=white" alt="SwiftUI">
  <img src="https://img.shields.io/badge/SwiftData-BE4041" alt="SwiftData">
  <img src="https://img.shields.io/badge/AVFoundation-BE4041" alt="AVFoundation">
  <img src="https://img.shields.io/badge/License-MIT-BE4041" alt="MIT">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/NeiroProjectX/.github/main/divider.png" width="320" height="6" alt="">
</p>

<p align="center">
  在喧嚣里，留一处安静的角落。Neiro 把 <a href="https://www.asmr.one">ASMR.ONE</a> 的海量作品装进 iOS 原生的质感里——<br>
  从指尖滑动的卡片转场，到深夜锁屏的一句轻语，每一处都为睡前那一刻而设计。
</p>

<p align="center">
  不托管任何音频，仅通过公开接口获取元数据与播放地址，<br>
  用 SwiftUI 从零构建流畅度、手势、后台与系统集成，做到 iOS 该有的样子。
</p>

<h3 align="center">核心特性</h3>

<table align="center">
  <tr>
    <td align="center">
      <strong>原生播放体验</strong><br>
      MiniPlayer · 全屏播放器 · 卡片转场 · 手势 · 倍速 · 循环模式
    </td>
    <td align="center">
      <strong>为睡前而生</strong><br>
      后台播放 · 锁屏控制 · 睡眠定时器 · 沉浸深色界面 · 画中画
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>字幕与悬浮歌词</strong><br>
      全屏字幕跟随 · 画中画歌词（实验性）· 单双行自适应排版
    </td>
    <td align="center">
      <strong>账户与云端同步</strong><br>
      Keychain 安全登录 · 收藏 / 评分 / 评论 · 播放列表创建与分享
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>结构化发现</strong><br>
      推荐 · 高级搜索与结构化候选 · 标签 / 声优 / 社团 · 相似作品
    </td>
    <td align="center">
      <strong>隐私与本地优先</strong><br>
      凭据不外泄 · 断点本机存储 · 头像按账户隔离 · 退出保留本地
    </td>
  </tr>
</table>

<p align="center">
  <img src="https://raw.githubusercontent.com/NeiroProjectX/.github/main/divider.png" width="320" height="6" alt="">
</p>

<h3 align="center">技术构成</h3>

<p align="center">
  <code>Swift 5.9</code> · <code>SwiftUI</code> · <code>AVFoundation / MediaPlayer</code> · <code>Observation</code> · <code>SwiftData</code> · <code>URLSession</code> · <code>CryptoKit / Keychain Services</code> · <code>XcodeGen</code><br>
  最低系统 iOS 17.0，无第三方包管理运行时依赖
</p>

<h3 align="center">源码结构</h3>

```text
NeiroApp/
├─ Sources/
│  ├─ App/             应用入口、根导航与环境注入
│  ├─ DesignSystem/    主题、图片加载与通用组件
│  ├─ Features/        首页 · 详情 · 播放器 · 搜索 · 账户 · 资料库
│  │   └─ Player/PiP/  悬浮歌词实验模块
│  ├─ Models/          API、播放与账户模型
│  └─ Services/        网络、认证、播放、同步与本地存储
└─ Resources/          App 图标与资源

project.yml            XcodeGen 工程定义
.github/workflows/     无签名 IPA 的 CI 构建
tools/                 构建及维护脚本
```

<h3 align="center">本地构建</h3>

<p align="center">
  需要 macOS、Xcode 16 或更高版本，以及 XcodeGen；或直接生成无签名 IPA（自行签名 / SideStore / AltStore 侧载）
</p>

```bash
brew install xcodegen && xcodegen generate && open Neiro.xcodeproj
./tools/build_unsigned_ipa.sh
```

<p align="center">
  <img src="https://raw.githubusercontent.com/NeiroProjectX/.github/main/divider.png" width="320" height="6" alt="">
</p>

<h3 align="center">数据 · 隐私 · 版权</h3>

<p align="center">
  登录凭据由 iOS Keychain 保存，项目不记录密码或令牌日志
<p align="center">
头像、播放断点和部分偏好仅保存在本机
</p>
<p align="center">
收藏、评分、评论、进度和播放列表写入用户自己的 ASMR.ONE 账户
</p>

<p align="center">
  Neiro 是独立的非官方客户端，与 ASMR.ONE、DLsite 及作品作者不存在隶属或授权关系。
</p>
<p align="center">
仓库代码许可不覆盖 ASMR.ONE 数据、作品封面、音频、字幕或其他第三方内容。
</p>

<h3 align="center">许可</h3>

<p align="center">
  Neiro 是独立的原生 Swift 项目，不包含任何第三方项目源码。<br>
  以 <a href="https://github.com/NeiroProjectX/Neiro/blob/main/LICENSE"><strong>MIT License</strong></a> 发布 · Copyright © 2026 NeiroProjectX
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/NeiroProjectX/.github/main/divider.png" width="320" height="6" alt="">
</p>

<p align="center">
  如果 Neiro 让你的夜晚更安静一点<br>
  <strong>欢迎 Star，关注后续更新</strong>
</p>
