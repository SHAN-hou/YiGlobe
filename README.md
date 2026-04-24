# YiGlobe 八卦星云图

3D 易经六十四卦可视化手机 APP（iOS / Android）

基于 Three.js 的 3D 球面卦象展示，使用 Capacitor 将完整 Web 应用打包为原生 APP。

## 功能

- 64 卦象分布在 3D 球面，支持触摸旋转、双指缩放
- 双击卦象弹出古图 + 详细爻辞
- 7 种动画运动模式（月令循环、螺旋、脉冲等）
- 搜索卦名/序号，点击飞向目标卦
- 灯箱放大查看释义图（双指缩放/拖动/双击重置）
- 4 个可拖动浮窗（控制面板/卦图/详情/说明）
- 完全离线运行，无需网络

## 在线预览

- https://shan-hou.github.io/yiglobe-mobile/

## 技术栈

- **Web 层**：Three.js r160 + CSS2DRenderer + ES Module Shims
- **原生层**：Capacitor 8 (WebView 嵌入)
- **平台**：Android (WebView) + iOS (WKWebView)

## 开发

### 环境要求

- Node.js >= 18
- Android Studio (Android 开发)
- Xcode 15+ (iOS 开发，需 macOS)

### 安装

```bash
npm install
```

### 同步原生项目

```bash
npx cap sync
```

### 运行

```bash
# Android
npx cap open android    # 在 Android Studio 中打开
npx cap run android     # 直接运行到设备/模拟器

# iOS (需 macOS)
npx cap open ios        # 在 Xcode 中打开
npx cap run ios         # 直接运行到设备/模拟器
```

### 构建发布

```bash
# Android APK/AAB
# 在 Android Studio: Build > Generate Signed Bundle/APK

# iOS IPA
# 在 Xcode: Product > Archive
```

## 项目结构

```
YiGlobe/
├── www/                          # Web 资源（Capacitor 服务目录）
│   ├── index.html                # 主页面（离线版）
│   ├── hexdetail.js              # 卦象详情面板
│   ├── lib/                      # Three.js r160 本地库
│   ├── AI命名卦图/                # 64 张卦象缩略图
│   └── hexagram_explanation_.../  # 59 张释义大图
├── android/                      # Android 原生项目
├── ios/                          # iOS 原生项目
├── capacitor.config.ts           # Capacitor 配置
└── package.json
```

## 许可

MIT
