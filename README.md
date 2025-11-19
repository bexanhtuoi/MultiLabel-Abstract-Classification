# Dự Án Phân Loại Đa Nhãn Bài Báo Khoa Học

## Giới thiệu
Dự án này nhằm xây dựng một hệ thống **phân loại đa nhãn** cho các bài báo khoa học dựa trên **Abstract** của bài báo. Hệ thống sẽ xác định xem một bài báo thuộc các lĩnh vực nào, ví dụ như:
- Computer Science
- Physics
- Mathematics
- Statistics
- Quantitative Biology
- Quantitative Finance

Mỗi bài báo có thể thuộc nhiều lĩnh vực cùng lúc, do đó đây là bài toán **đa nhãn (multi-label classification)**.

## Dataset
- Dataset bao gồm các bài báo với **Abstract** và **Title**, cùng với các nhãn (labels) tương ứng.
- Giá trị `1` trong cột nhãn thể hiện bài báo thuộc nhãn đó, giá trị `0` thể hiện không thuộc.
- Dataset được sử dụng từ **Analytics Vidhya Hackathon**.

### Ví dụ cấu trúc dataset

| Title | Abstract | Computer Science | Physics | Mathematics | Statistics | Quantitative Biology | Quantitative Finance |
|-------|----------|----------------|---------|-------------|-----------|--------------------|--------------------|
| ...   | ...      | 1              | 0       | 0           | 1         | 0                  | 0                  |

## Mục tiêu
1. Tiền xử lý dữ liệu: làm sạch text, tokenization, embedding.
2. Xây dựng mô hình phân loại đa nhãn dựa trên **Abstract**.
3. Đánh giá mô hình bằng các metric phù hợp với đa nhãn như **Micro F1**, **Macro F1**, **Hamming Loss**.
4. Cho phép dự đoán nhãn cho các bài báo mới dựa trên Abstract.

## Công nghệ sử dụng
- Python 3.x
- Thư viện NLP: `transformers`, `sentence-transformers`, `scikit-learn`, `pandas`, `numpy`
- Thư viện đánh giá: `scikit-learn`
- Môi trường thực hiện: **Google Colab / Jupyter Notebook**

