---
layout: post
title: Extension - Tạo chuỗi JSON từ Data
tags:
  - iOS
  - extension
  - Data
---

Bạn có `Data` và bạn muốn tạo một `String` với format dạng JSON từ nó? Đơn giản chỉ để `print` cái `String` ấy ra xem cho dễ chẳng hạn.

---

Hãy tạo một extension cho `Data`:

```swift
extension Data {
    var jsonString: String? {
        get {
            if let json = String(data: self, encoding: String.Encoding.utf8) {
                return json
            }
            
            return nil
        }
    }
}
```

Sau đó, ta có thể sử dụng nó như sau:

```swift
let data = // #Your data
        
print("JSON string: \(data.jsonString)")
```