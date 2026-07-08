# 16. Compression

## Mục Tiêu

- Giảm kích thước model checkpoint.
- Giữ chất lượng mô hình trong ngưỡng chấp nhận.

## Kiến Thức Cốt Lõi

- Pruning có cấu trúc và không cấu trúc.
- Sparsity và fine-tuning sau pruning.

## Ý Nghĩa Trong ML

- Compression giúp tiết kiệm lưu trữ và giảm băng thông triển khai.

## Triển Khai Đề Xuất

- Cài magnitude pruning cơ bản.
- Fine-tune ngắn sau pruning để phục hồi chất lượng.
- Báo cáo compression ratio.

## Tối Ưu Nên Làm

- Chọn mức sparsity tăng dần theo lịch, tránh prune quá mạnh ngay từ đầu.

## Checklist

- Kích thước checkpoint giảm có số liệu.
- Model sau nén vẫn suy luận đúng.
