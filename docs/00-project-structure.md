# 00. Cấu Trúc Dự Án Và Lộ Trình Kỹ Thuật

Tài liệu này trả lời câu hỏi: nên tổ chức file như thế nào khi tự xây lại PyTorch từ đầu, và nên tối ưu ở giai đoạn nào.

## Mục Tiêu Thiết Kế

- Dễ đọc, dễ test, dễ mở rộng.
- Tách rõ tầng toán học (ops, autograd) và tầng API (nn, optim, data).
- Hỗ trợ thay backend tính toán (CPU trước, GPU sau).

## Cấu Trúc Thư Mục Đề Xuất

```text
src/tini_torch/
  tensor/            # Tensor object, shape/stride, dtype, view ops
  ops/               # Primitive ops: add, mul, matmul, reduce, broadcast
  autograd/          # Computation graph, backward engine, grad accumulation
  nn/
    modules/         # Linear, Conv2d, LayerNorm, Dropout, Transformer blocks
    functional/      # relu, softmax, cross_entropy, ...
  optim/             # SGD, Momentum, Adam, schedulers
  data/              # Dataset, DataLoader, collation
  backends/          # CPU backend trước; GPU backend sau

tests/
  unit/              # Test logic đơn vị
  grad/              # Gradient check (finite difference)
  integration/       # Train loop end-to-end

examples/            # Script minh hoạ train/infer
benchmarks/          # Kịch bản đo hiệu năng
scripts/             # Công cụ hỗ trợ (format, test, benchmark)
docs/                # Tài liệu lộ trình
```

## Thứ Tự Implement Khuyến Nghị

1. `tensor` + `ops`:
   - Scalar, vector, matrix, n-d tensor.
   - Shape, size, stride, broadcasting.
2. `autograd`:
   - Graph node, topological backward, grad accumulation.
3. `nn` + `optim` + `data`:
   - Layer/loss/optimizer và training loop.
4. Mở rộng kiến trúc:
   - CNN, attention, transformer.
5. Tối ưu hệ thống:
   - Profiling trước, tối ưu sau.

## Có Nên Gọi Thư Viện Tối Ưu Phần Cứng Ngay Không?

Khuyến nghị:
- Giai đoạn đầu: không cần.
- Lý do: cần chắc correctness, API và test trước.
- Sau khi có benchmark và điểm nghẽn rõ ràng mới tối ưu bằng:
  - Vectorized kernels.
  - Caching/memoization.
  - Quantization/compression.
  - Backend tăng tốc (CUDA, custom kernels) nếu thực sự cần.

## Tiêu Chí Hoàn Thành Theo Giai Đoạn

- Đúng: test pass và gradient check pass.
- Ổn định: chạy lặp lại ra kết quả gần tương đương.
- Đủ nhanh: có benchmark baseline và cải thiện định lượng.