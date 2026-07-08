# 10. Tokenization

## Mục Tiêu

- Chuyển văn bản thô thành chuỗi token ID cho mô hình.
- Quản lý từ điển và token đặc biệt rõ ràng.

## Kiến Thức Cốt Lõi

- Vocabulary và tần suất từ.
- Token đặc biệt: `<pad>`, `<unk>`, `<bos>`, `<eos>`.
- Chiến lược token hóa: whitespace, subword, BPE cơ bản.

## Ý Nghĩa Trong ML

- Chất lượng tokenization ảnh hưởng trực tiếp đến chất lượng mô hình NLP.

## Triển Khai Đề Xuất

- Cài `fit`, `encode`, `decode`.
- Hỗ trợ truncation và padding theo max length.
- Lưu/đọc tokenizer config để tái sử dụng.

## Tối Ưu Nên Làm

- Cache kết quả tokenization cho tập train lặp lại nhiều epoch.

## Checklist

- Encode/decode nhất quán với text trong-vocab.
- Batch token có shape đồng nhất.
