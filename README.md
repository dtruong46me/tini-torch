# tini-torch

`tini-torch` là dự án học thuật để tự xây dựng lại một thư viện deep learning theo tinh thần PyTorch, đi từ phần nhỏ nhất (tensor, shape, scalar, autograd) đến các mô hình lớn hơn (CNN, Transformer), rồi tối ưu hiệu năng.

## Tổng Quan Dự Án

Mục tiêu chính:
- Hiểu bản chất toán học và kỹ thuật của deep learning framework.
- Tự triển khai pipeline huấn luyện hoàn chỉnh.
- Biết cách đánh đổi giữa đúng đắn, tốc độ và bộ nhớ.
- Có nền tảng để mở rộng lên backend CPU/GPU và kernel tối ưu.

Bạn sẽ xây dựng theo nhiều lớp:
1. Lõi Tensor + Autograd.
2. API mạng nơ-ron (layer, loss, optimizer, dataloader).
3. Kiến trúc mô hình (Conv, Attention, Transformer).
4. Tối ưu hệ thống (profiling, quantization, compression, acceleration).

## Yêu Cầu Môi Trường

| Nhóm | Yêu cầu tối thiểu | Gợi ý |
|---|---|---|
| Python | 3.10+ | 3.11+ |
| Quản lý gói | pip 23+ | venv hoặc conda |
| Thư viện dev | pytest | numpy, matplotlib, jupyter, ruff, mypy |
| Phần cứng | CPU 2 core, RAM 8 GB | RAM 16 GB, GPU CUDA (tuỳ chọn) |

Cài nhanh bộ công cụ cơ bản:

```bash
pip install numpy pytest matplotlib jupyter ruff mypy
```

## Sẽ Build Những Gì?

| Mã | Chủ đề | Kết quả đầu ra | Tài liệu |
|---|---|---|---|
| 00 | Tổng quan cấu trúc | Cấu trúc thư mục và quyết định kiến trúc | [docs/00-project-structure.md](docs/00-project-structure.md) |
| 01-08 | Foundation | Tensor core, autograd, layer, loss, optimizer, training loop | [docs/foundation/00-tier-overview.md](docs/foundation/00-tier-overview.md) |
| 09-13 | Architecture | CNN mini, tokenizer, embedding, attention, transformer mini | [docs/architecture/00-tier-overview.md](docs/architecture/00-tier-overview.md) |
| 14-19 | Optimization | Profiling, quantization, compression, acceleration, benchmark | [docs/optimization/00-tier-overview.md](docs/optimization/00-tier-overview.md) |
| 20 | Capstone | Bài thi tổng hợp Torch Olympics | [docs/capstone/00-competition-overview.md](docs/capstone/00-competition-overview.md) |

## Mục Lục Docs

Tài liệu tổng hợp nằm tại [docs/index.md](docs/index.md).

Có thể xem `index.md` ngay từ README bằng bảng link nhanh bên dưới:

| Tier | Link |
|---|---|
| Foundation | [docs/foundation/00-tier-overview.md](docs/foundation/00-tier-overview.md) |
| Architecture | [docs/architecture/00-tier-overview.md](docs/architecture/00-tier-overview.md) |
| Optimization | [docs/optimization/00-tier-overview.md](docs/optimization/00-tier-overview.md) |
| Capstone | [docs/capstone/00-competition-overview.md](docs/capstone/00-competition-overview.md) |

## Cấu Trúc Repository

Khung thư mục hiện tại để bắt đầu implement:

```text
src/tini_torch/
	tensor/
	autograd/
	nn/
		modules/
		functional/
	optim/
	data/
	ops/
	backends/
tests/
	unit/
	grad/
	integration/
examples/
benchmarks/
scripts/
docs/
```

## Ghi Chú Về Tối Ưu Backend

Khi xây lại framework từ đầu, lộ trình hợp lý là:
1. Làm đúng trước (correctness-first), có test và grad-check.
2. Tối ưu sau bằng vectorization, cache, quantization.
3. Chỉ khi cần mới chuyển sang kernel mức thấp hoặc backend phần cứng chuyên biệt.

Nói ngắn gọn: không cần gọi thư viện tối ưu phần cứng ngay từ đầu; nên xây lõi rõ ràng trước rồi tối ưu theo dữ liệu benchmark.

## License

Xem [LICENSE](LICENSE).
