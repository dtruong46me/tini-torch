# 01. Tensor

## Mục Tiêu

- Hiểu tensor là đơn vị dữ liệu cốt lõi trong machine learning.
- Tự cài `Tensor` gồm storage, dtype, shape, stride và metadata gradient.
- Nắm rõ cách shape/size ảnh hưởng trực tiếp đến phép toán và hiệu năng.

## Kiến Thức Cốt Lõi

- Scalar: tensor bậc 0, shape `()`.
- Vector: tensor bậc 1, shape ví dụ `(d,)`.
- Matrix: tensor bậc 2, shape `(m, n)`.
- N-d tensor: tensor nhiều chiều, ví dụ ảnh `(B, C, H, W)`.

Thuật ngữ quan trọng:
- `shape`: kích thước từng chiều.
- `rank`: số chiều (số phần tử trong `shape`).
- `size`: tổng số phần tử (tích các chiều).
- `stride`: bước nhảy bộ nhớ theo từng chiều.

## Ý Nghĩa Trong ML

- Mọi phép tính học sâu đều là phép toán trên tensor.
- Quản lý shape đúng giúp tránh lỗi logic mô hình.
- Tối ưu stride/layout giúp tăng tốc đáng kể trên CPU/GPU.

## Triển Khai Đề Xuất

1. Cài `Tensor` data model:
   - `data`, `shape`, `dtype`, `stride`, `requires_grad`, `grad`.
2. Cài primitive ops:
   - `add`, `sub`, `mul`, `div`, `matmul`.
3. Cài view ops:
   - `reshape`, `transpose`, `flatten`, `squeeze`, `unsqueeze`.
4. Cài broadcasting theo quy tắc tương thích chiều từ phải sang trái.

## Tối Ưu Nên Làm

- Ưu tiên view thay vì copy dữ liệu.
- Tránh tạo tensor tạm không cần thiết.
- Chuẩn hóa layout để cache locality tốt hơn.

## Checklist

- Kết quả toán học khớp với NumPy.
- Bắt lỗi shape mismatch rõ ràng.
- Test đủ edge case: scalar, tensor rỗng, broadcast nhiều chiều.
