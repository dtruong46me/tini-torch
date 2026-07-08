# 09. Convolutions

## Mục Tiêu

- Cài `Conv2d` và pooling đủ dùng cho CNN cơ bản.
- Hiểu rõ stride, padding, dilation và receptive field.

## Kiến Thức Cốt Lõi

- Convolution là phép tích chập theo cửa sổ trượt.
- Output shape phụ thuộc `kernel_size`, `stride`, `padding`.
- Pooling giảm độ phân giải để giảm chi phí tính toán.

## Ý Nghĩa Trong ML

- CNN học đặc trưng cục bộ và chia sẻ trọng số hiệu quả.
- Convolution là nền cho hầu hết tác vụ thị giác truyền thống.

## Triển Khai Đề Xuất

- Cài forward/backward cho `Conv2d`.
- Cài `MaxPool2d` hoặc `AvgPool2d`.
- Viết shape test cho nhiều cấu hình stride/padding.

## Tối Ưu Nên Làm

- Bắt đầu bằng bản dễ hiểu, sau đó tối ưu bằng `im2col + matmul`.
- Tránh vòng lặp Python sâu trên từng pixel nếu có thể.

## Checklist

- Kết quả khớp baseline ở toy input.
- Gradient check pass cho convolution weight/input.
