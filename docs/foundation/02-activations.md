# 02. Activations

## Mục Tiêu

- Cài các hàm kích hoạt phổ biến và gradient tương ứng.
- Hiểu tác động của activation đến khả năng hội tụ.

## Kiến Thức Cốt Lõi

- Sigmoid và tanh: mượt nhưng dễ bão hòa.
- ReLU: nhanh, đơn giản, có thể gây dead neurons.
- LeakyReLU/GELU: cải thiện gradient flow trong nhiều bài toán.

## Ý Nghĩa Trong ML

- Activation tạo phi tuyến, giúp mô hình học quan hệ phức tạp.
- Chọn activation phù hợp giúp train ổn định hơn.

## Triển Khai Đề Xuất

- Cài `relu`, `sigmoid`, `tanh`, `gelu`.
- Cài backward rule rõ ràng cho từng hàm.
- Viết test numeric gradient cho các điểm biên.

## Tối Ưu Nên Làm

- Dùng kernel vectorized cho ops elementwise.
- Tránh tính lại biểu thức forward không cần thiết ở backward.

## Checklist

- Forward khớp giá trị tham chiếu.
- Gradient pass finite-difference check.
