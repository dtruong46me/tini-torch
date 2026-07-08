# 12. Attention

## Mục Tiêu

- Cài scaled dot-product attention và mask.
- Mở rộng lên multi-head attention.

## Kiến Thức Cốt Lõi

- Chiếu tuyến tính sang `Q`, `K`, `V`.
- Điểm attention: `QK^T / sqrt(d_k)`.
- Dùng mask cho causal LM và padding.

## Ý Nghĩa Trong ML

- Attention cho phép mô hình học quan hệ phụ thuộc xa trong chuỗi.

## Triển Khai Đề Xuất

- Cài single-head trước, sau đó multi-head.
- Cài softmax ổn định số với masking.
- Test tách riêng causal mask và padding mask.

## Tối Ưu Nên Làm

- Fused path cho `matmul + mask + softmax` nếu cần tăng tốc.
- Giảm tensor tạm để tiết kiệm bộ nhớ.

## Checklist

- Hành vi causal đúng (không nhìn tương lai).
- Shape output đúng cho nhiều head.
