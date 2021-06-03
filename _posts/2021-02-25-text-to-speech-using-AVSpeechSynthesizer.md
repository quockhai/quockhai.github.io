---
layout: post
title: Text-To-Speech đơn giản với AVSpeechSynthesizer
tags:
  - iOS
  - speech
  - AVFoundation
---

Sử dụng `AVSpeechSynthesizer` để làm tính năng Text-To-Speech một cách hết sức đơn giản.

Đầu tiên, import `AVFoundation`:

```swift
import AVFoundation
```

Tạo và sử dụng `AVSpeechSynthesizer`:

```swift
let utterance = AVSpeechUtterance(string: "Hello world")
utterance.voice = AVSpeechSynthesisVoice(language: "en-GB")
utterance.rate = 0.5 

let synthesizer = AVSpeechSynthesizer()
synthesizer.speak(utterance)
```

Với `AVSpeechSynthesisVoice` bạn có thể chọn ngôn ngữ `language` và giọng đọc `identifier` (VD: `com.apple.ttsbundle.Samantha-compact` cho giọng của Samantha).