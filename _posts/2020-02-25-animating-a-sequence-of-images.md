---
layout: post
title: Tạo animation với một chuỗi các hình ảnh
tags:
  - iOS
  - animation
---

`UIImage` ngoài việc đặt một ảnh tĩnh, còn có thể tạo animation với một chuỗi các hình ảnh, hay không?

Đơn giản, chỉ cần truyền vào một mảng các images và đặt duration cho chúng. Hãy làm như sau:

**Cách 1:**

```swift
imageView.image = UIImage.animatedImage(with: images, duration: 2.0)
```

**Cách 2:**

```swift
imageView.animationImages = images
imageView.animationDuration = 2.0

imageView.startAnimating()
```