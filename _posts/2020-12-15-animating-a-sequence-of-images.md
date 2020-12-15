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
imageView.image = UIImage.animatedImage(with: images, duration: 2.0)
```

**OR**

```swift
imageView.animationImages = images
imageView.animationDuration = 2.0

imageView.startAnimating()
```