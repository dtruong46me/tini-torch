# 03. Layers

## Mục Tiêu

- Xây API `Module` theo hướng dễ mở rộng.
- Quản lý tham số tự động cho mô hình nhiều lớp.

## Kiến Thức Cốt Lõi

- `Linear`: biến đổi affine cơ bản.
- `Dropout`: regularization trong mode train.
- `LayerNorm`: ổn định huấn luyện chuỗi/transformer.

## Ý Nghĩa Trong ML

- Layer là khối xây dựng chính của mọi kiến trúc.
- Thiết kế module tốt giúp giảm lỗi khi mở rộng model.

## Triển Khai Đề Xuất

- Cài `Module` base với `forward`, `__call__`, `parameters`, `train/eval`.
- Cài `Linear` trước, sau đó thêm `Dropout`, `LayerNorm`.
- Hỗ trợ module lồng nhau và tự động duyệt tham số.

## Tối Ưu Nên Làm

- Chọn init phù hợp (Xavier/He).
- Hạn chế tạo object tạm trong forward path.

## Checklist

- Shape output đúng theo thiết kế.
- `parameters()` thu thập đủ toàn bộ tham số.
