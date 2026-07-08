# 14. Profiling

## Mục Tiêu

- Xác định đúng bottleneck về thời gian và bộ nhớ.
- Ưu tiên tối ưu dựa trên dữ liệu, không dựa trên cảm giác.

## Kiến Thức Cốt Lõi

- Wall time, CPU time, memory allocation.
- Hot path trong forward/backward.
- Khác biệt giữa latency và throughput.

## Ý Nghĩa Trong ML

- Profiling là điểm bắt đầu bắt buộc trước mọi tối ưu lớn.

## Triển Khai Đề Xuất

- Tạo script profiling cho train step và inference step.
- Ghi top op tốn thời gian nhất.
- Ghi đỉnh bộ nhớ và pattern cấp phát.

## Tối Ưu Nên Làm

- Chỉ tối ưu top bottleneck.
- So sánh trước/sau trên cùng cấu hình benchmark.

## Checklist

- Có báo cáo profiler lặp lại được.
- Có danh sách bottleneck có thứ tự ưu tiên.
