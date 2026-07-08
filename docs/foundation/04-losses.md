# 04. Losses

## Mục Tiêu

- Cài các hàm loss chính cho regression và classification.
- Đảm bảo loss ổn định số cho dữ liệu thực tế.

## Kiến Thức Cốt Lõi

- `MSE` cho bài toán hồi quy.
- `CrossEntropy` cho phân loại nhiều lớp.
- Kỹ thuật `log-sum-exp` để tránh tràn số.

## Ý Nghĩa Trong ML

- Loss định nghĩa mục tiêu học của mô hình.
- Sai công thức hoặc kém ổn định sẽ làm gradient không tin cậy.

## Triển Khai Đề Xuất

- Cài `mse_loss`, `cross_entropy`.
- Hỗ trợ reduction `none/sum/mean`.
- Ưu tiên `log_softmax + nll` cho cross-entropy.

## Tối Ưu Nên Làm

- Fused computation cho softmax + CE để giảm bộ nhớ tạm.

## Checklist

- Khớp baseline NumPy/PyTorch ở test mẫu.
- Không phát sinh `nan/inf` ở logits lớn.
