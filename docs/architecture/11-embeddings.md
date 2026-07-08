# 11. Embeddings

## Mục Tiêu

- Ánh xạ token ID sang vector liên tục.
- Cộng thông tin vị trí cho chuỗi đầu vào.

## Kiến Thức Cốt Lõi

- Embedding lookup table có trainable weights.
- Positional encoding: learned hoặc sinusoidal.

## Ý Nghĩa Trong ML

- Embedding là cầu nối giữa dữ liệu rời rạc và không gian liên tục để học.

## Triển Khai Đề Xuất

- Cài `Embedding(num_embeddings, embedding_dim)`.
- Cài positional embedding hoặc sinusoidal encoding.
- Cộng token embedding + positional embedding trước khi vào block attention.

## Tối Ưu Nên Làm

- Tránh gather rời rạc quá nhiều lần không cần thiết.
- Tối ưu memory layout để truy xuất embedding nhanh.

## Checklist

- Output shape đúng `(B, T, D)`.
- Positional encoding cho kết quả xác định.
