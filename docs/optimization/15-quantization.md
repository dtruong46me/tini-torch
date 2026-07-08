# 15. Quantization

## Mục Tiêu

- Giảm độ chính xác số để tăng tốc và giảm bộ nhớ.
- Đo trade-off accuracy so với latency/throughput.

## Kiến Thức Cốt Lõi

- Quantization int8 với scale/zero-point.
- Post-training quantization và quantization-aware training (mức nâng cao).

## Ý Nghĩa Trong ML

- Quantization đặc biệt hữu ích khi triển khai model trên thiết bị tài nguyên hạn chế.

## Triển Khai Đề Xuất

- Bắt đầu với post-training quantization cho một số layer chính.
- So sánh accuracy và tốc độ với FP32 baseline.

## Tối Ưu Nên Làm

- Calibrate trên tập đại diện để giảm sai số lượng tử hóa.

## Checklist

- Model quantized chạy end-to-end.
- Chênh lệch accuracy nằm trong ngưỡng chấp nhận.
