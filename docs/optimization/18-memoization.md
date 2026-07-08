# 18. Memoization

## Mục Tiêu

- Tránh tính toán lặp lại cho các nhánh xử lý quyết định.
- Đánh đổi hợp lý giữa RAM và thời gian chạy.

## Kiến Thức Cốt Lõi

- Cache key, cache value, eviction policy.
- Hit rate và miss rate.

## Ý Nghĩa Trong ML

- Hữu ích cho bước tiền xử lý hoặc phép tính deterministic lặp lại nhiều lần.

## Triển Khai Đề Xuất

- Chọn một điểm tính toán lặp để cache.
- Gắn metric hit/miss.
- Đảm bảo invalidation đúng khi input thay đổi.

## Tối Ưu Nên Làm

- Giới hạn kích thước cache để tránh chiếm RAM quá mức.

## Checklist

- Hit rate đủ cao để có lợi ích thực tế.
- Kết quả cache không làm sai logic mô hình.
