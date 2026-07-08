# 08. Training

## Mục Tiêu

- Ghép toàn bộ thành pipeline huấn luyện đầy đủ.
- Theo dõi metric và checkpoint để tái lập thí nghiệm.

## Kiến Thức Cốt Lõi

- Chu kỳ train: forward -> loss -> backward -> step.
- Tách train/eval mode.
- Logging theo epoch và step.

## Ý Nghĩa Trong ML

- Đây là điểm kiểm thử toàn bộ framework trong điều kiện thực tế.

## Triển Khai Đề Xuất

- Cài `Trainer` tối thiểu cho train/eval.
- Log loss, accuracy, thời gian epoch.
- Lưu checkpoint gồm model + optimizer + trạng thái train.

## Tối Ưu Nên Làm

- Gradient clipping cho bài toán dễ bùng gradient.
- Chỉ bật mixed precision sau khi lõi đã ổn định.

## Checklist

- Train loss giảm ổn định.
- Khôi phục từ checkpoint và train tiếp thành công.
