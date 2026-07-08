# 19. Benchmarking

## Mục Tiêu

- Thiết kế benchmark công bằng và tái lập.
- So sánh baseline với bản tối ưu có cơ sở.

## Kiến Thức Cốt Lõi

- Warmup và đo steady-state.
- Độ lệch chuẩn giữa các lần chạy.
- Chỉ số: latency, throughput, memory, accuracy.

## Ý Nghĩa Trong ML

- Benchmark là bằng chứng khách quan cho quyết định kỹ thuật.

## Triển Khai Đề Xuất

- Cố định seed, data split, phần cứng, batch size.
- Chạy nhiều lần và lấy thống kê trung bình.
- Lưu kết quả vào bảng so sánh nhất quán.

## Tối Ưu Nên Làm

- Tách benchmark micro (op-level) và macro (end-to-end).

## Checklist

- Benchmark chạy lại cho kết quả ổn định.
- Báo cáo có đầy đủ metadata môi trường.
