# 00. Tổng Quan Architecture Tier

Architecture tier đưa framework từ mức primitive lên mức mô hình hiện đại dùng cho CV và NLP.

## Mục Tiêu

- Cài các khối kiến trúc then chốt: convolution, embedding, attention, transformer.
- Đảm bảo các khối này train được end-to-end bằng lõi đã xây ở Foundation.

## Phạm Vi

- `09` Convolutions
- `10` Tokenization
- `11` Embeddings
- `12` Attention
- `13` Transformers

## Tiêu Chí Hoàn Thành Tier

- Train được một CNN nhỏ.
- Train được một transformer nhỏ trên tác vụ toy sequence.
- Unit test và shape test đầy đủ cho từng block.
