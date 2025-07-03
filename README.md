# 📘 Báo cáo môn Khai phá dữ liệu

> Tiểu luận tổng hợp kiến thức về 3 kỹ thuật trọng yếu trong lĩnh vực Data Mining:
> - Phân lớp với **Random Forest**
> - Phân cụm với **DBSCAN**
> - Luật kết hợp với **FP-Growth**

---

## 👨‍🎓 Thông tin sinh viên

- **Họ tên**: Võ Lê Thiên Ân  
- **MSSV**: 74802302849  
- **Lớp**: 23HTDL  
- **Giảng viên hướng dẫn**: TS. Trương Hải Bằng  
- **Học kỳ**: HK2 – Năm học 2024–2025

---

## 🧠 Nội dung chính

### 1️⃣ Phân lớp – Phát hiện gian lận thẻ tín dụng bằng Random Forest

- **Thuật toán**: Random Forest (Ensemble Learning)
- **Mục tiêu**: Phân loại giao dịch hợp lệ và giao dịch gian lận.
- **Dữ liệu**: Bộ dữ liệu Credit Card Fraud Detection từ Kaggle (284,807 giao dịch).
- **Kỹ thuật xử lý**:
  - Cân bằng dữ liệu bằng SMOTE.
  - Đánh giá mô hình bằng AUPRC, F1-score, Precision/Recall.
- **Kết quả nổi bật**:
  - Precision (gian lận): 0.98, Recall: 0.91
  - AUPRC = 0.96
  - Accuracy tổng thể: 95.73%
- **So sánh mô hình**: RF vượt trội hơn SVC (94.97%) và CNN (92.33%).

✅ *Random Forest thể hiện hiệu quả cao, khả năng tổng quát tốt, đặc biệt phù hợp với bài toán mất cân bằng dữ liệu.*

---

### 2️⃣ Phân cụm – Phân khúc khách hàng bằng DBSCAN

- **Thuật toán**: DBSCAN (Density-Based Clustering)
- **Mục tiêu**: Phân nhóm khách hàng theo tiêu chí chi tiêu, thu nhập và độ tuổi.
- **Dữ liệu**: Customer Segmentation từ Kaggle (200 khách hàng).
- **Tiền xử lý**:
  - Chuẩn hóa dữ liệu (MinMaxScaler).
  - Loại bỏ nhiễu và ngoại lệ.
- **Tham số DBSCAN**: `eps = 0.1209`, `minPts = 4`
- **Kết quả phân cụm**:
  - Số cụm: 4 + nhóm nhiễu (-1)
  - Silhouette Score: 0.6737 (cao nhất)
  - Davies-Bouldin Index: 0.4726 (thấp nhất)

✅ *DBSCAN phát hiện được cả cụm có hình dạng phức tạp và điểm ngoại lệ — điều mà KMeans và CLARANS không làm tốt.*

---

### 3️⃣ Luật kết hợp – Phân tích giỏ hàng bằng FP-Growth

- **Thuật toán**: FP-Growth (Frequent Pattern Mining)
- **Mục tiêu**: Khai thác các sản phẩm thường được mua cùng nhau để gợi ý bán hàng.
- **Dữ liệu**: Groceries Dataset (~38.000 giao dịch siêu thị).
- **Phương pháp**:
  - Xây dựng FP-Tree từ tập giao dịch.
  - Trích xuất Frequent Itemsets.
  - Sinh luật kết hợp dựa trên chỉ số Support, Confidence, Lift.
- **Ứng dụng**:
  - Gợi ý mua hàng (cross-selling).
  - Thiết kế chương trình khuyến mãi.
  - Tối ưu trưng bày sản phẩm.

✅ *FP-Growth tối ưu hóa hiệu suất hơn Apriori, đặc biệt với tập dữ liệu lớn và dày đặc.*

---

## ⚙️ Tổng quan thuật toán

| Thuật toán       | Nhóm      | Điểm mạnh chính                                                | Điểm hạn chế chính                                 |
|------------------|-----------|------------------------------------------------------------------|----------------------------------------------------|
| Random Forest    | Phân lớp  | Chính xác cao, chống overfitting, không cần chuẩn hóa dữ liệu    | Khó diễn giải, chi phí tính toán cao               |
| DBSCAN           | Phân cụm  | Tự động xác định số cụm, xử lý tốt nhiễu và cụm bất thường       | Nhạy cảm với `eps`, kém hiệu quả khi dữ liệu nhiều chiều |
| FP-Growth        | Luật kết hợp | Tốc độ nhanh, không sinh tập ứng viên, hiệu quả với dữ liệu lớn | Cấu trúc phức tạp, không phù hợp với dữ liệu động |

---

## 📎 Tài liệu tham khảo

1. [Kaggle - Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
2. [Kaggle - Customer Segmentation Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
3. Groceries Dataset for Market Basket Analysis
4. Nhiều bài báo khoa học được trích dẫn trong báo cáo chính thức.


