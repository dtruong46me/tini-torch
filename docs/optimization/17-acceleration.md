# 17. Acceleration

## Mục Tiêu

- Tăng tốc các đoạn code tốn thời gian nhất.
- Cải thiện throughput hoặc giảm latency theo mục tiêu.

## Kiến Thức Cốt Lõi

- Vectorization thay cho vòng lặp Python.
- Batch processing.
- Tối ưu memory access pattern.

## Ý Nghĩa Trong ML

- Tăng tốc giúp thử nghiệm nhanh hơn và giảm chi phí compute.

## Triển Khai Đề Xuất

- Chuyển op nóng sang dạng vectorized.
- Gộp các op liên tiếp khi hợp lý.
- Đo lại benchmark sau từng thay đổi.

## Tối Ưu Nên Làm

- Ưu tiên thay đổi đơn giản nhưng tác động lớn trước.

## Checklist

- Có speedup định lượng trước/sau.
- Tối ưu không làm sai kết quả số học.
