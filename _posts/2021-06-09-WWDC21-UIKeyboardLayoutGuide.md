---
layout: post
title: WWDC21 - UIKeyboardLayoutGuide
tags:
  - wwdc21
  - ios
  - keyboard
---

Xử lý các vấn đề liên quan đến `keyboard` lúc nào cũng là một công việc tốn thời gian với nhiều chi tiết lặt vặt.

Lần này, ở WWDC21 với iOS 15, có vẻ Apple đã lắng nghe và trợ giúp các lập trình viên xử lý vấn đề này với `UIKeyboardLayoutGuide`.

Giờ đây, ngoài `safeAreaLayoutGuide`, chúng ta có thêm `keyboardLayoutGuide`, như ví dụ dưới đây:

```swift
inputView.bottomAnchor.constraint(equalTo: view.keyboardLayoutGuide.topAnchor).isActive = true
```

Với dòng lệnh trên, `inputView` sẽ luôn luôn nằm phía trên của `keyboard`. Quá hay!