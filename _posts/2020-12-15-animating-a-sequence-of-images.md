---
layout: post
title: Animating A Sequence of Images
tags:
  - iOS
  - animation
---

You can create a repeating "flip book" or animated gif effect given multiple images.

With `images` and `duration` like this:

```swift
UIImage.animatedImage(with: images, duration: 2.0)
```