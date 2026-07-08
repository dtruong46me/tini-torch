# Tài Liệu tini-torch

Tài liệu này mô tả lộ trình xây dựng lại một framework deep learning từ đầu theo phong cách PyTorch.

## 00. Khởi Tạo Dự Án

- [00. Cấu trúc dự án và lộ trình kỹ thuật](00-project-structure.md)

## Foundation Tier

- [00. Tổng quan Foundation](foundation/00-tier-overview.md)
- [01. Tensor](foundation/01-tensor.md)
- [02. Activations](foundation/02-activations.md)
- [03. Layers](foundation/03-layers.md)
- [04. Losses](foundation/04-losses.md)
- [05. DataLoader](foundation/05-dataloader.md)
- [06. Autograd](foundation/06-autograd.md)
- [07. Optimizers](foundation/07-optimizers.md)
- [08. Training](foundation/08-training.md)

## Architecture Tier

- [00. Tổng quan Architecture](architecture/00-tier-overview.md)
- [09. Convolutions](architecture/09-convolutions.md)
- [10. Tokenization](architecture/10-tokenization.md)
- [11. Embeddings](architecture/11-embeddings.md)
- [12. Attention](architecture/12-attention.md)
- [13. Transformers](architecture/13-transformers.md)

## Optimization Tier

- [00. Tổng quan Optimization](optimization/00-tier-overview.md)
- [14. Profiling](optimization/14-profiling.md)
- [15. Quantization](optimization/15-quantization.md)
- [16. Compression](optimization/16-compression.md)
- [17. Acceleration](optimization/17-acceleration.md)
- [18. Memoization](optimization/18-memoization.md)
- [19. Benchmarking](optimization/19-benchmarking.md)

## Capstone Tier

- [00. Competition Overview](capstone/00-competition-overview.md)
- [20. Torch Olympics](capstone/20-torch-olympics.md)

## Kết Quả Mong Đợi

Sau khi hoàn thành toàn bộ lộ trình, bạn có thể:
- Tự xây tensor engine và autograd hoạt động đúng.
- Tự build/training model không phụ thuộc internals của PyTorch.
- Đo và tối ưu hiệu năng có phương pháp.
- Trình bày kết quả bằng benchmark và tài liệu tái lập.