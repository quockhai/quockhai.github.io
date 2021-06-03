---
layout: post
title: Extension - Kiểm tra một ngày bất kỳ có phải hôm nay
tags:
  - iOS
  - extension
  - Date
---

`Calendar` có một hàm rất hay và đơn giản để kiểm tra xem một ngày bất kỳ có phải ngày hôm nay hay không:

```swift
Calendar.current.isDateInToday(date)
```

---

Để cho đơn giản, hãy tạo một extension cho `Date`:

```swift
extension Date {
    var isToday: Bool {
        get {
            return Calendar.current.isDateInToday(self)
        }
    }
}

```

Sau đó, ta có thể sử dụng nó như sau:

```swift
let date = // #Your date
        
if date.isToday {
	// #Code
}
```

Rất hay phải không nào ^^