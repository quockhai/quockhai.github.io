---
layout: post
title: Text to speech using AVSpeechSynthesizer
tags:
  - iOS
  - speech
---

Using `AVSpeechSynthesizer` to convert text to speech in easy way.

1. First, import `AVFoundation` to your class:

```swift
import AVFoundation
```

2. Create and using `AVSpeechSynthesizer`:

```swift
let utterance = AVSpeechUtterance(string: "Hello world")
utterance.voice = AVSpeechSynthesisVoice(language: "en-GB")
utterance.rate = 0.5 

let synthesizer = AVSpeechSynthesizer()
synthesizer.speak(utterance)
```

You can custom `AVSpeechSynthesisVoice` with `language` or `identifier` (ex: `com.apple.ttsbundle.Samantha-compact` for Samantha voice).