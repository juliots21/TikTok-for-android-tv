# TikTok TV (Sleppify)

An optimized TikTok wrapper for Android TV that brings the full desktop experience to the big screen with enhanced remote control support, layout fixes, and seamless Google authentication.

## 🚀 Key Features

### 🎮 Advanced Remote Control Support
- **DPad Navigation**: Fully optimized scrolling and sidebar interactions (Up/Down for feed, Left/Right for menus).
- **Virtual Mouse (Magic Remote Style)**: Long-press the **OK** button to toggle a physics-based cursor. It allows interacting with elements not reachable via standard D-Pad focus.
- **Context-Aware Sidebar**: Intelligent detection of the currently centered video to ensure "Like", "Comment", and "Share" buttons always target the correct content.

### 🔐 Google Sign-in Fix
- Custom WebView implementation that handles Google authentication gracefully by dynamically switching between User Agents and suppressing interference scripts during the OAuth flow. No more "Browser not supported" errors.

### 🖼️ Display & Layout Optimizations
- **Desktop UI Enforcement**: Forces the full desktop site for a premium TV experience, avoiding the limitations of the mobile site.
- **Viewport Scaling**: Automatic adjustment of CSS rules to prevent UI clipping and ensure buttons are properly sized for TV viewports.
- **Anti-Black Screen Fixes**: CSS injections that handle hardware acceleration edge cases on Android TV.

## 🛠️ Tech Stack
- **Native Android**: Kotlin-based `MainActivity` managing the `WebView` lifecycle and input event dispatching.
- **JavaScript Bridge**: Custom bridge (`tiktok_tv_bridge.js`) that injects layouts, manages scroll states, and provides context for the remote control.
- **Physics Engine**: Smooth acceleration and friction logic for the virtual mouse movement.

## 📂 Project Structure
- `app/src/main/java/.../MainActivity.kt`: Entry point, input handling, and WebView configuration.
- `app/src/main/assets/tiktok_tv_bridge.js`: The "brain" injected into TikTok to enable TV-specific behaviors.
- `app/src/main/res/layout/activity_main.xml`: Fullscreen WebView container.

## ⚙️ Installation
1. Clone the repository.
2. Open with Android Studio.
3. Build and deploy to an Android TV device or emulator.

---
Created with ❤️ by [juliots21](https://github.com/juliots21)
