---
layout: post
title:  "How to copy text to the clipboard using UIPasteboard"
date:   2019-05-28 21:03:36 +0530
categories: iOS Swift
---
You can write to and read from the iOS clipboard by using the **UIPasteboard** class, which has a **generalPasteboard()** method that returns the shared system method of copying and pasting data between apps. Using this you can write text to the clipboard just like this:

```swift
let pasteboard = UIPasteboard.general
pasteboard.string = "Hello, world!"
```

To read text back from the clipboard, you should unwrap its optional value like this:
```swift
if let string = pasteboard.string {
    // text was found and placed in the "string" constant
}
```
