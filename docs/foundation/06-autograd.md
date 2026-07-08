# 06. Autograd

## Mục Tiêu

- Xây reverse-mode autodiff cho graph động.
- Đảm bảo gradient đúng với graph có nhánh và tham số dùng lại.

## Kiến Thức Cốt Lõi

- Chain rule đa biến.
- Sắp topo cho backward.
- Cộng dồn gradient trên node chung.

## Ý Nghĩa Trong ML

- Autograd quyết định trực tiếp khả năng học của mô hình.

## Triển Khai Đề Xuất

- Tensor lưu `parents`, `grad_fn`, `requires_grad`.
- `backward()` duyệt ngược topo và cộng dồn gradient.
- Có `no_grad` context cho inference hoặc update thủ công.

## Tối Ưu Nên Làm

- Giải phóng graph không cần thiết để giảm RAM.
- Cân bằng giữa cache trung gian và chi phí tính lại.

## Checklist

- Pass finite-difference cho op chính.
- Gradient cộng dồn đúng ở shared subgraph.
