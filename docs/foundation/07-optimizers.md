# 07. Optimizers

## Mục Tiêu

- Cài thuật toán cập nhật tham số cốt lõi.
- Quản lý state optimizer để train ổn định.

## Kiến Thức Cốt Lõi

- SGD, Momentum, Adam.
- Learning rate, weight decay, bias correction.

## Ý Nghĩa Trong ML

- Optimizer ảnh hưởng mạnh đến tốc độ hội tụ và chất lượng nghiệm cuối.

## Triển Khai Đề Xuất

- Base class `Optimizer` với `param_groups`.
- Cài `step()` và `zero_grad()` chuẩn.
- Cài `SGD`, `Adam` trước khi thêm scheduler.

## Tối Ưu Nên Làm

- Update in-place khi an toàn.
- State dict rõ ràng để lưu/khôi phục checkpoint.

## Checklist

- Loss giảm trên toy task.
- Resume từ checkpoint vẫn hội tụ liên tục.
