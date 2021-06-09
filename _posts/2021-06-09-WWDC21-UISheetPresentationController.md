---
layout: post
title: WWDC21 - UISheetPresentationController
tags:
  - wwdc21
  - ios
---

WWDC21 với rất nhiều thay đổi trên iOS 15 và `UISheetPresentationController` là một trong số đó.

Với `UISheetPresentationController` anh em có thể custom nhiều hơn cách hiển thị một `viewController`. Cùng khám phá nào ^^

Bắt đầu với một hàm khởi tạo mặc định:

```swift
func showSheetViewController() {
    let sheetViewController = KTSheetViewController(nibName: nil, bundle: nil)
   
    present(sheetViewController, animated: true, completion: nil)
}
```

Anh em có thể đặt size mặc định cho `KTSheetViewController ` trong hàm `viewDidLoad`:

```swift
override func viewDidLoad() {
    super.viewDidLoad()
    
    if let presentationController = presentationController as? UISheetPresentationController {
        presentationController.detents = [.medium(), .large()]
    }
}
```

Và lựa chọn chọn ẩn/hiển `grabber`:

```swift
if let presentationController = presentationController as? UISheetPresentationController {
	presentationController.detents = [.medium(), .large()]
	presentationController.prefersGrabberVisible = true
}
```
Với sự hỗ trợ của `UISheetPresentationController`, anh em sẽ tiết kiệm được rất nhiều công sức cho việc vẽ các `UIViewController`, thời gian đó dành để tập trung xử lý logic và các công việc khác hữu ích hơn ^^
