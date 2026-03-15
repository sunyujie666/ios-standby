# 🕐 StandBy Mode

iOS 风格的待机时钟 PWA，将手机横放即可变身智能床头钟。

![StandBy](web/icon-192.png)

## ✨ 功能特性

- **🕐 实时时钟** — 大字体时间显示，附带日期和秒数
- **⏰ 快捷闹钟** — 5/10/30/60 分钟快捷设定 + 自定义时长，倒计时进度环
- **👁 注视感知** — 前置摄像头检测人脸，看一眼亮屏 5 分钟，无人时自动变暗
- **🌤 实时天气** — 基于 GPS 定位，显示温度、湿度、天气状况（30 分钟自动刷新）
- **🌙 红色夜间模式** — 一键切换低蓝光模式，保护夜间视力
- **⚡ 低电量模式** — 关闭动画，降低检测频率，延长续航
- **📷 摄像头定时** — 可设置 1~8 小时后自动关闭摄像头，之后交由系统息屏
- **📱 PWA 支持** — 添加到主屏幕，全屏运行，脱离浏览器体验
- **🔒 屏幕常亮** — Wake Lock API + NoSleep fallback，确保不息屏
- **📐 强制横屏** — 竖屏时自动 CSS 旋转，始终保持横屏显示

## 🚀 快速开始

### 在线使用

直接用 Safari 打开页面，点击 **"分享 → 添加到主屏幕"**，即可获得全屏 PWA 体验。

### 本地运行

```bash
# 克隆仓库
git clone https://github.com/your-username/ios-standby.git
cd ios-standby

# 启动本地服务器（任选其一）
npx serve web
# 或
python3 -m http.server 8000 -d web
```

然后用浏览器访问 `http://localhost:8000`（或 `http://localhost:3000`）。

## 📁 项目结构

```
ios-standby/
└── web/
    ├── index.html      # 主页面（HTML + CSS + JS 单文件）
    ├── manifest.json   # PWA 清单
    ├── icon-192.png    # 应用图标 192×192
    └── icon-512.png    # 应用图标 512×512
```

## 🛠 技术栈

- **纯原生** HTML / CSS / JavaScript，零依赖
- **FaceDetector API**（Chrome）+ 运动检测 fallback（Safari）
- **Web Audio API** 闹钟音效（兼容 iOS Safari）
- **Wake Lock API** + NoSleep 视频 hack 保持屏幕常亮
- **Open-Meteo API** 免费天气数据
- **PWA** manifest + 全屏模式

## 📱 兼容性

| 平台 | 浏览器 | 注视感知 |
|------|--------|---------|
| iOS | Safari (PWA) | ✅ 运动检测 |
| Android | Chrome | ✅ FaceDetector API |
| Desktop | Chrome / Edge | ✅ FaceDetector API |
| Desktop | Safari / Firefox | ✅ 运动检测 fallback |

## 📄 License

MIT
