# 00. Tổng Quan Foundation Tier

Foundation là tầng quan trọng nhất: nếu tầng này không chắc, các tầng trên sẽ sai hoặc khó tối ưu.

## Mục Tiêu

- Xây dựng lõi tensor đúng về toán học và shape semantics.
- Cài đặt autograd đủ để huấn luyện model cơ bản.
- Hoàn thiện pipeline tối thiểu: data -> model -> loss -> backward -> optimizer.

## Phạm Vi

- `01` Tensor
- `02` Activations
- `03` Layers
- `04` Losses
- `05` DataLoader
- `06` Autograd
- `07` Optimizers
- `08` Training

## Tiêu Chí Hoàn Thành Tier

- Unit test pass cho các primitive chính.
- Gradient check pass cho các phép toán có đạo hàm.
- Train được ít nhất một mô hình nhỏ với loss giảm ổn định.

## Lỗi Thường Gặp

- Broadcasting sai chiều.
- Tích lũy gradient sai khi graph có nhánh.
- Mất ổn định số ở `softmax` và `cross_entropy`.
- Quên phân biệt mode train/eval.
