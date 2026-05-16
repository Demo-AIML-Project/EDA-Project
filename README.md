# 📊 Toàn Diện Kiến Thức: Trực Quan Hóa Dữ Liệu và EDA

## Chủ đề 0: Data Visualization & EDA
### (Matplotlib • Seaborn • Phân tích dữ liệu • Biểu đồ)

---

# 📖 1. Khái niệm EDA là gì?

EDA (Exploratory Data Analysis) là quá trình phân tích khám phá dữ liệu trước khi xây dựng mô hình Machine Learning.

## 🎯 Mục tiêu của EDA

- Hiểu dữ liệu
- Tìm missing values
- Phát hiện outlier
- Kiểm tra phân phối dữ liệu
- Phân tích correlation
- Tìm pattern dữ liệu
- Kiểm tra imbalance dataset
- Chuẩn bị dữ liệu cho ML

---

# 📌 2. Cốt lõi của EDA

EDA giúp trả lời các câu hỏi:

| Câu hỏi | Ý nghĩa |
|---|---|
| Dữ liệu có sạch không? | Missing / duplicate |
| Có outlier không? | Giá trị bất thường |
| Phân phối dữ liệu thế nào? | Gaussian / skew |
| Feature nào quan trọng? | Correlation |
| Dataset có imbalance không? | Bias model |
| Có pattern gì không? | Xu hướng dữ liệu |

---

# 📌 3. Pipeline EDA chuẩn thực tế

```text
Load Data
↓
Check Shape
↓
Check Missing Values
↓
Check Data Types
↓
Statistics Summary
↓
Visualization
↓
Correlation Analysis
↓
Outlier Detection
↓
Feature Understanding
↓
Preprocessing
↓
Train Model
```

---

# 📌 4. Matplotlib là gì?

Matplotlib là thư viện visualization nền tảng trong Python.

## 📌 Dùng để:

- Vẽ biểu đồ
- Trực quan hóa dữ liệu
- Phân tích dữ liệu
- Debug ML model
- Dashboard cơ bản

## 📌 Import

```python
import matplotlib.pyplot as plt
```

---

# 📌 5. Seaborn là gì?

Seaborn là thư viện visualization được xây dựng trên Matplotlib.

## 📌 Ưu điểm

- Đẹp hơn
- Code ngắn hơn
- Hỗ trợ thống kê mạnh
- Tối ưu cho EDA

## 📌 Import

```python
import seaborn as sns
```

---

# 📌 6. Matplotlib vs Seaborn

| Matplotlib | Seaborn |
|---|---|
| Low-level | High-level |
| Tuỳ biến mạnh | Visualization đẹp |
| Code dài hơn | Code ngắn hơn |
| Khó hơn | Dễ dùng hơn |
| Linh hoạt cao | Tối ưu EDA |

---

# 📌 7. Những biểu đồ quan trọng nhất trong ML

---

## 7.1 Histogram

### 📌 Mục đích

Dùng để xem phân phối dữ liệu.

### 📌 Ví dụ

```python
plt.hist(df["salary"])
plt.show()
```

### 📌 Giúp phát hiện

- Gaussian distribution
- Right skew
- Left skew
- Bất thường dữ liệu

---

## 7.2 Boxplot

### 📌 Mục đích

Dùng để detect outlier.

### 📌 Ví dụ

```python
sns.boxplot(x=df["price"])
plt.show()
```

### 📌 Ý nghĩa

- Điểm nằm xa hộp = outlier

---

## 7.3 Scatter Plot

### 📌 Mục đích

Phân tích mối quan hệ giữa 2 biến.

### 📌 Ví dụ

```python
plt.scatter(df["area"], df["price"])
plt.show()
```

### 📌 Dùng để

- Kiểm tra linear relationship
- Detect cluster
- Detect outlier

---

## 7.4 Heatmap

### 📌 Mục đích

Hiển thị correlation matrix.

### 📌 Ví dụ

```python
sns.heatmap(df.corr(), annot=True)
plt.show()
```

### 📌 Rất quan trọng cho

- Feature Selection
- Multicollinearity

---

## 7.5 Countplot

### 📌 Mục đích

Kiểm tra imbalance dataset.

### 📌 Ví dụ

```python
sns.countplot(x=df["label"])
plt.show()
```

---

## 7.6 Pairplot

### 📌 Mục đích

Xem quan hệ tổng thể giữa các feature.

### 📌 Ví dụ

```python
sns.pairplot(df)
plt.show()
```

---

# 📌 8. Missing Values

## 📌 Kiểm tra

```python
df.isnull().sum()
```

## 📌 Ảnh hưởng

- Model lỗi
- Accuracy giảm
- Bias dữ liệu

## 📌 Cách xử lý

- Drop rows
- Mean
- Median
- Mode
- Predict missing values

---

# 📌 9. Duplicate Data

## 📌 Kiểm tra

```python
df.duplicated().sum()
```

## 📌 Ảnh hưởng

- Overfitting
- Sai thống kê

---

# 📌 10. Outlier

## 📖 Khái niệm

Outlier là dữ liệu bất thường.

Ví dụ:
- Nhà giá quá cao
- Lương bất thường
- Sensor lỗi

## 📌 Ảnh hưởng

Đặc biệt nguy hiểm với:
- Linear Regression
- Logistic Regression
- Statistical models

---

# 📌 11. Distribution

## 📖 Phân phối dữ liệu

Một số loại phổ biến:

- Normal Distribution
- Right Skew
- Left Skew

## 📌 Tại sao quan trọng?

Nhiều model ML hoạt động tốt hơn với dữ liệu gần Gaussian.

---

# 📌 12. Correlation

## 📖 Khái niệm

Correlation thể hiện mức độ liên quan giữa các feature.

## 📌 Kiểm tra

```python
df.corr()
```

## 📌 Ý nghĩa

| Giá trị | Ý nghĩa |
|---|---|
| 1 | Liên quan mạnh cùng chiều |
| -1 | Liên quan mạnh ngược chiều |
| 0 | Không liên quan |

---

# 📌 13. Multicollinearity

## 📖 Khái niệm

Khi nhiều feature chứa thông tin giống nhau.

## 📌 Ảnh hưởng

Đặc biệt xấu với:
- Linear Regression
- Logistic Regression

## 📌 Giải pháp

- Remove feature
- PCA
- Feature Selection

---

# 📌 14. Feature Scaling

## 📖 Vai trò trong EDA

EDA giúp phát hiện:
- Feature scale quá chênh lệch

Ví dụ:

| Feature | Value |
|---|---|
| age | 20 |
| salary | 1000000 |

---

## 📌 Model cần scaling

- KNN
- SVM
- Logistic Regression
- Neural Network

## 📌 Model ít cần scaling

- Random Forest
- XGBoost

---

# 📌 15. EDA ảnh hưởng model như thế nào?

EDA ảnh hưởng trực tiếp tới:

- Accuracy
- Overfitting
- Underfitting
- Feature Quality
- Training Speed
- Stability của model

---

# 📌 16. Workflow EDA thực tế

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load data
df = pd.read_csv("data.csv")

# Basic info
print(df.shape)
print(df.info())
print(df.describe())

# Missing values
print(df.isnull().sum())

# Histogram
df.hist(figsize=(12,8))

# Correlation
sns.heatmap(df.corr(), annot=True)

# Outlier
sns.boxplot(x=df["price"])

plt.show()
```

---

# 📌 17. Khi nào dùng từng biểu đồ?

| Biểu đồ | Dùng khi |
|---|---|
| Histogram | Xem phân phối |
| Boxplot | Detect outlier |
| Scatter Plot | Quan hệ 2 biến |
| Heatmap | Correlation |
| Countplot | Imbalance |
| Line Chart | Time Series |
| Pairplot | Dataset nhỏ |

---

# 📌 18. EDA trong dự án thực tế

## 🏠 House Price Prediction

EDA kiểm tra:
- Giá nhà
- Diện tích
- Correlation
- Outlier
- Distribution

---

## 📧 Spam Email Detection

EDA kiểm tra:
- Imbalance
- Từ xuất hiện nhiều
- Độ dài email
- Pattern spam

---

## 👥 Customer Churn

EDA kiểm tra:
- Hành vi khách hàng
- Correlation với churn
- Nhóm khách dễ rời bỏ

---

# 📌 19. Những lỗi phổ biến người mới mắc

| Lỗi | Hậu quả |
|---|---|
| Không check missing | Model lỗi |
| Không detect outlier | Accuracy thấp |
| Không visualize | Không hiểu data |
| Không check imbalance | Bias model |
| Chỉ train model | Không hiểu dataset |
| Không xem correlation | Feature dư thừa |

---

# 📌 20. Kiến thức thực chiến cần vững

## 🔥 Bắt buộc phải biết

- Histogram
- Boxplot
- Heatmap
- Correlation
- Missing values
- Outlier
- Distribution
- Imbalance dataset
- Feature Scaling

---

# 📌 21. Lộ trình học đúng

```text
Pandas
↓
Matplotlib
↓
Seaborn
↓
EDA Project
↓
Feature Engineering
↓
Machine Learning
```

---

# 📌 22. Project nên thực hành

## 📌 Beginner

- Titanic Dataset
- House Price Analysis
- Sales Analysis

## 📌 Intermediate

- Customer Churn
- Spam Email Analysis

## 📌 Advanced

- Financial Data Analysis
- Real-time Dashboard
- ML Monitoring

---

# 📌 23. Tư duy đúng trong thực tế

Một AI Engineer / Data Scientist tốt sẽ:

- Không train model ngay
- Luôn EDA trước
- Hiểu dữ liệu trước khi optimize model
- Visualization để hiểu business
- Tập trung dataset quality

👉 Dataset tốt thường quan trọng hơn model mạnh.

---

# 🚀 Tổng Kết

EDA và Data Visualization là nền tảng cực kỳ quan trọng trong:

- Machine Learning
- Data Science
- AI Engineering
- Data Analysis

Một người mạnh EDA thường:
- Debug model nhanh hơn
- Feature engineering tốt hơn
- Hiểu dữ liệu sâu hơn
- Làm dự án thực tế hiệu quả hơn

---

# 🛠️ Công nghệ liên quan

## 📌 Libraries phổ biến

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn

---

# 📚 Tài liệu nên học tiếp

Sau chủ đề này nên học:

1. Pandas nâng cao
2. Feature Engineering
3. Statistics for ML
4. Machine Learning Algorithms
5. Data Cleaning thực chiến
6. Dashboard & BI

---

# 🎯 Mục tiêu cuối cùng

Biết cách:

- Đọc dataset
- Hiểu dataset
- Tìm vấn đề dataset
- Visualize dữ liệu đúng
- Chuẩn bị dữ liệu cho Machine Learning
- Làm EDA như người đi làm thực tế

