# flutter_ffmpeg_utils

A Flutter plugin to execute raw FFmpeg commands on Android and iOS.

## 🚀 Features
- Run **raw FFmpeg commands** directly on Android and iOS.
- Supports complex media operations such as trimming, merging, and transcoding.
- Fully compatible with `mobile-ffmpeg` on Android and `ffmpeg-kit-ios-full` on iOS.

---

## 📦 Installation
Add the following to your `pubspec.yaml`:
```yaml
dependencies:
  ffmpeg_utils: ^1.0.0
```

Run:
```bash
flutter pub get
```

---

## ⚡️ Usage
```dart
import 'package:ffmpeg_utils/ffmpeg_utils.dart';

final ffmpegUtils = FfmpegUtils();

// Run a raw FFmpeg command
await ffmpegUtils.executeFFmpeg(['-i', 'input.mp4', '-vf', 'scale=640:480', 'output.mp4']);
```

---

## 📚 Examples

### 1. Compress a Video
```dart
await ffmpegUtils.executeFFmpeg(['-i', 'input.mp4', '-vcodec', 'libx264', '-crf', '28', 'output.mp4']);
```

### 2. Trim a Video
```dart
await ffmpegUtils.executeFFmpeg(['-i', 'input.mp4', '-ss', '00:00:10', '-to', '00:00:20', '-c', 'copy', 'output.mp4']);
```

### 3. Extract Audio from Video
```dart
await ffmpegUtils.executeFFmpeg(['-i', 'input.mp4', '-vn', '-acodec', 'libmp3lame', 'output.mp3']);
```

---

## 🎯 Supported Platforms
- ✅ Android
- ✅ iOS

---

## 📝 License
MIT License. See `LICENSE` for details.
