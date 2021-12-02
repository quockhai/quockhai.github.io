---
layout: post
title: CGAffineTransform - Bound vs. Frame
tags:
  - bound
  - frame
  - ios
---

Chào anh em,

Lâu lâu mới lại có bài hầu chuyện anh em. Mấy tháng vừa rồi mình bận quá, nhiều công việc, nhiều dự án, nhiều kiến thức và lĩnh vực mới cần lĩnh ngộ.

Đợt này thì vẫn bận như vậy thôi, nhưng mình sẽ cố gắng quay lại viết bài đều đặn hơn, cố gắng mỗi tuần ra 1-2 bài nhỏ nhỏ chia sẻ với anh em ;)

Cụ thể, hôm nay mình gặp vấn đề với `CGAffineTransform`, mình dùng hàm `CGAffineTransformMakeRotation` để xoay một view. Việc xoay thì rất OK, nhưng kết quả không mong muốn là khi xoay thì size của view cũng bị thay đổi.

Vò đầu bứt tai cả ngày trời mà không tìm ra phương án giải quyết. Mãi vừa xong mới tìm được manh mối:

> Changes to this property can be animated. However, if the transform property contains a non-identity transform, the value of the frame property is undefined and should not be modified. In that case, you can reposition the view using the center property and adjust the size using the bounds property instead.

Đây là đoạn lưu ý về `frame` trong Apple Documentation.

Vậy đó, nếu có vấn đề với `size` khi sử dụng `CGAffineTransform`, thì hãy dùng `bound` thay cho `frame` - rất hay phải không?

Cám ơn anh em.
