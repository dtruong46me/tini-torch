# 13. Transformers

## Mục Tiêu

- Ghép attention và MLP thành transformer block hoàn chỉnh.
- Train được mô hình chuỗi nhỏ end-to-end.

## Kiến Thức Cốt Lõi

- Residual connections + normalization.
- MLP block sau attention.
- Kiến trúc encoder-only và decoder-only.

## Ý Nghĩa Trong ML

- Transformer là kiến trúc cốt lõi của NLP hiện đại và nhiều tác vụ đa phương thức.

## Triển Khai Đề Xuất

- Cài block: `LayerNorm -> MHA -> residual -> LayerNorm -> MLP -> residual`.
- Stack nhiều block thành model.
- Thêm hàm generate cơ bản cho decoder-only.

## Tối Ưu Nên Làm

- Chia nhỏ batch/sequence khi memory giới hạn.
- Dùng cache key/value khi sinh token tự hồi quy.

## Checklist

- Logits shape đúng `(B, T, vocab_size)`.
- Model overfit được tập chuỗi nhỏ để xác nhận correctness.
