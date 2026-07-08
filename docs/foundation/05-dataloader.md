# 05. DataLoader

## Mục Tiêu

- Thiết kế tầng dữ liệu ổn định cho train/eval.
- Hỗ trợ batching, shuffle và tái lập kết quả.

## Kiến Thức Cốt Lõi

- `Dataset`: truy xuất mẫu đơn.
- `DataLoader`: iterator sinh mini-batch.
- `collate_fn`: quy tắc ghép batch.

## Ý Nghĩa Trong ML

- Data pipeline tốt giúp tận dụng tài nguyên tính toán hiệu quả.
- Shuffle/seed chuẩn giúp đánh giá mô hình công bằng hơn.

## Triển Khai Đề Xuất

- Cài interface `Dataset` (`__len__`, `__getitem__`).
- Cài `DataLoader` với `batch_size`, `shuffle`, `drop_last`.
- Hỗ trợ seed cố định cho chạy tái lập.

## Tối Ưu Nên Làm

- Tối ưu `collate_fn` để giảm copy.
- Cân nhắc prefetch/caching theo workload.

## Checklist

- Batch shape nhất quán.
- Cùng seed cho cùng thứ tự dữ liệu.
