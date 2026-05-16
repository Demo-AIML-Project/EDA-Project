# 📊 COMPLETE README — Data Visualization & EDA Foundation

# Chủ đề 0: Trực quan hóa dữ liệu và EDA
## (Pandas • NumPy • Matplotlib • Seaborn • Data Analysis • Visualization)

---

# 📖 Giới thiệu

Đây là bộ kiến thức nền tảng cực kỳ quan trọng trước khi học:

- Machine Learning
- Data Science
- AI Engineering
- Data Analysis
- Deep Learning

Bộ công cụ này giúp:

- Hiểu dữ liệu
- Phân tích dữ liệu
- Làm sạch dữ liệu
- Trực quan hóa dữ liệu
- Chuẩn bị dữ liệu cho ML
- Debug model
- Tạo báo cáo dữ liệu

---

# 🧠 Tổng quan hệ sinh thái

| Công cụ | Vai trò |
|---|---|
| NumPy | Nền tảng toán học |
| Pandas | Xử lý dữ liệu |
| Matplotlib | Visualization cơ bản |
| Seaborn | Visualization thống kê |
| EDA | Hiểu dữ liệu trước ML |

---

# 📌 1. EDA là gì?

EDA (Exploratory Data Analysis)
= Phân tích khám phá dữ liệu.

---

## 🎯 Mục tiêu của EDA

EDA giúp:

- Hiểu dataset
- Tìm vấn đề dữ liệu
- Detect outlier
- Check missing values
- Phân tích correlation
- Kiểm tra imbalance dataset
- Hiểu pattern dữ liệu
- Chuẩn bị dữ liệu trước ML

---

# 📌 2. Tư duy cốt lõi của EDA

```text
Hiểu dữ liệu trước khi train model
```

Người mới thường:
- train model trước
- optimize model trước

Nhưng thực tế:
- dataset quality quan trọng hơn model.

---

# 📌 3. NumPy toàn diện

# NumPy là gì?

NumPy = Numerical Python.

Là thư viện xử lý:

- array
- vector
- matrix
- linear algebra
- toán học tốc độ cao

---

# 📌 Vì sao NumPy quan trọng?

Machine Learning thật sự là:

- vector
- matrix
- tensor
- thống kê
- linear algebra

NumPy là nền tảng cho toàn bộ phần này.

---

# 📌 NumPy dùng trong ML để làm gì?

| Công việc | Vai trò |
|---|---|
| Matrix operations | Cực kỳ quan trọng |
| Statistics | Mean / Std |
| Optimization | Gradient |
| Vectorization | Tăng tốc |
| Linear algebra | ML core |

---

# 📌 Ví dụ NumPy

```python
import numpy as np

arr = np.array([1,2,3])

print(arr)
```

---

# 📌 Kiến thức NumPy bắt buộc

## Phải biết:

- array
- shape
- reshape
- slicing
- indexing
- broadcasting
- vectorization
- matrix multiplication

---

# 📌 NumPy trong thực tế

NumPy được dùng trong:

- Machine Learning
- Deep Learning
- Computer Vision
- NLP
- Data Science

Rất nhiều framework build dựa trên tư duy NumPy.

---

# 📌 4. Pandas toàn diện

# Pandas là gì?

Pandas là thư viện xử lý dữ liệu mạnh nhất Python.

---

# 📌 Pandas dùng để làm gì?

| Công việc | Vai trò |
|---|---|
| Read CSV/Excel | Load dataset |
| Cleaning | Làm sạch dữ liệu |
| Filtering | Lọc dữ liệu |
| Merge | Nối bảng |
| Missing Values | Xử lý null |
| Feature Engineering | Chuẩn bị ML |
| Groupby | Thống kê |

---

# 📌 DataFrame là gì?

DataFrame:
- giống Excel table
- nhưng mạnh hơn rất nhiều.

---

# 📌 Ví dụ Pandas

```python
import pandas as pd

df = pd.read_csv("data.csv")

print(df.head())
```

---

# 📌 Những hàm Pandas quan trọng

## Kiểm tra dữ liệu

```python
print(df.info())
print(df.describe())
```

---

## Missing values

```python
df.isnull().sum()
```

---

## Filtering

```python
df[df["salary"] > 5000]
```

---

## Groupby

```python
df.groupby("department").mean()
```

---

# 📌 Pandas trong thực tế

Pandas gần như bắt buộc trong:

- Data Analysis
- AI Engineering
- ML Engineering
- Data Science

---

# 📌 5. Visualization là gì?

Visualization:

```text
Biến dữ liệu thành hình ảnh
```

Mục tiêu:

- hiểu pattern
- hiểu xu hướng
- detect vấn đề
- report dữ liệu
- giải thích model

---

# 📌 6. Matplotlib toàn diện

# Matplotlib là gì?

Matplotlib là thư viện visualization nền tảng trong Python.

---

# 📌 Dùng để:

- Vẽ biểu đồ
- Visualization ML
- Monitoring model
- Training visualization
- Technical report

---

# 📌 Import Matplotlib

```python
import matplotlib.pyplot as plt
```

---

# 📌 Những biểu đồ quan trọng

| Chart | Dùng khi |
|---|---|
| Line Plot | Xu hướng |
| Bar Chart | So sánh |
| Histogram | Distribution |
| Scatter Plot | Correlation |
| Pie Chart | Tỷ lệ |

---

# 📌 Line Plot

```python
plt.plot(x, y)
plt.show()
```

Dùng cho:

- Time series
- Accuracy/loss
- Monitoring

---

# 📌 Histogram

```python
plt.hist(df["age"])
plt.show()
```

Dùng để:

- xem phân phối dữ liệu
- detect skew
- hiểu dataset

---

# 📌 Scatter Plot

```python
plt.scatter(df["area"], df["price"])
plt.show()
```

Dùng để:

- correlation
- cluster
- outlier

---

# 📌 Bar Chart

```python
plt.bar(names, values)
plt.show()
```

---

# 📌 Custom biểu đồ

## Title

```python
plt.title("Sales Report")
```

---

## Label

```python
plt.xlabel("Month")
plt.ylabel("Revenue")
```

---

## Grid

```python
plt.grid(True)
```

---

## Save figure

```python
plt.savefig("chart.png")
```

---

# 📌 Matplotlib trong ML

Dùng để visualize:

- train loss
- validation loss
- accuracy
- prediction result
- confusion matrix

---

# 📌 7. Seaborn toàn diện

# Seaborn là gì?

Seaborn là thư viện visualization được xây dựng trên Matplotlib.

---

# 📌 Ưu điểm của Seaborn

- đẹp hơn
- code ngắn hơn
- tối ưu EDA
- mạnh về thống kê

---

# 📌 Boxplot

```python
sns.boxplot(x=df["salary"])
```

Dùng để:
- detect outlier

---

# 📌 Heatmap

```python
sns.heatmap(df.corr(), annot=True)
```

Dùng để:
- correlation analysis
- feature selection

---

# 📌 Pairplot

```python
sns.pairplot(df)
```

Dùng để:
- xem quan hệ tổng thể giữa các feature.

---

# 📌 8. Correlation

# Correlation là gì?

Correlation = mức độ liên quan giữa features.

---

# 📌 Giá trị correlation

| Giá trị | Ý nghĩa |
|---|---|
| 1 | Liên quan mạnh |
| -1 | Ngược chiều mạnh |
| 0 | Không liên quan |

---

# 📌 Tại sao correlation quan trọng?

Giúp:

- feature selection
- detect multicollinearity
- hiểu dataset

---

# 📌 9. Missing Values

# Missing values là gì?

Dữ liệu bị thiếu.

Ví dụ:
- tuổi bị null
- salary trống

---

# 📌 Kiểm tra missing

```python
df.isnull().sum()
```

---

# 📌 Ảnh hưởng

- model lỗi
- accuracy giảm
- bias dữ liệu

---

# 📌 Cách xử lý

- drop
- mean
- median
- mode
- prediction filling

---

# 📌 10. Outlier

# Outlier là gì?

Dữ liệu bất thường.

Ví dụ:
- lương quá cao
- tuổi bất thường
- sensor lỗi

---

# 📌 Ảnh hưởng của outlier

- bias model
- loss tăng
- accuracy giảm
- regression bị ảnh hưởng mạnh

---

# 📌 Detect outlier

```python
sns.boxplot(x=df["salary"])
```

---

# 📌 11. Distribution

# Distribution là gì?

Phân phối dữ liệu.

---

# 📌 Các loại phổ biến

| Distribution | Ý nghĩa |
|---|---|
| Normal | Gaussian |
| Right Skew | Lệch phải |
| Left Skew | Lệch trái |

---

# 📌 Vì sao distribution quan trọng?

Nhiều model ML hoạt động tốt hơn khi dữ liệu gần Gaussian.

---

# 📌 12. Feature Scaling

# Feature Scaling là gì?

Chuẩn hóa scale dữ liệu.

Ví dụ:

| Feature | Value |
|---|---|
| age | 20 |
| salary | 1000000 |

---

# 📌 Model cần scaling

- KNN
- SVM
- Logistic Regression
- Neural Network

---

# 📌 Model ít cần scaling

- Random Forest
- XGBoost

---

# 📌 13. Workflow EDA thực tế

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load data

df = pd.read_csv("data.csv")

# Basic info
print(df.info())
print(df.describe())

# Missing values
print(df.isnull().sum())

# Correlation
sns.heatmap(df.corr(), annot=True)

# Distribution
plt.hist(df["age"])

# Outlier
sns.boxplot(x=df["salary"])

plt.show()
```

---

# 📌 14. Quan hệ giữa các thư viện

```text
NumPy
↓
Pandas build trên NumPy
↓
Matplotlib visualize data
↓
Seaborn enhance visualization
↓
EDA
↓
Machine Learning
```

---

# 📌 15. Pipeline ML thực tế

```text
Load Data
↓
Pandas xử lý dữ liệu
↓
EDA
↓
Visualization
↓
Feature Engineering
↓
Convert NumPy arrays
↓
Train ML model
```

---

# 📌 16. Những lỗi người mới thường gặp

| Lỗi | Hậu quả |
|---|---|
| Không check null | Model lỗi |
| Không EDA | Không hiểu data |
| Không visualize | Bỏ lỡ pattern |
| Không scaling | Model kém |
| Chỉ train model | Không hiểu dataset |
| Không detect outlier | Accuracy thấp |

---

# 📌 17. Trong thực tế đi làm

# Data Analyst

Dùng:

- Pandas
- Seaborn
- Matplotlib

---

# AI Engineer

Dùng:

- NumPy
- Pandas
- Visualization
- ML pipeline

---

# ML Engineer

NumPy rất quan trọng.

---

# 📌 18. Thứ tự học đúng

```text
Python
↓
NumPy
↓
Pandas
↓
Matplotlib
↓
Seaborn
↓
EDA
↓
Machine Learning
```

---

# 📌 19. Project nên thực hành

# Beginner

- Titanic EDA
- Sales Analysis
- Student Score Analysis

---

# Intermediate

- House Price Analysis
- Customer Churn
- Spam Email Analysis

---

# Advanced

- ML Dashboard
- Financial Analysis
- Real-time Monitoring

---

# 📌 20. Kiến thức thực chiến cần cực vững

## Bắt buộc:

- NumPy arrays
- Pandas DataFrame
- Missing values
- Correlation
- Histogram
- Heatmap
- Boxplot
- Feature Scaling
- Visualization
- EDA workflow

---

# 📌 21. Tư duy đúng trong thực tế

Người mới thường nghĩ:

```text
Model là quan trọng nhất
```

Nhưng thực tế:

```text
Data > Model
```

---

# 📌 22. Tổng kết

## NumPy

= nền tảng toán học của ML.

---

## Pandas

= nền tảng xử lý dữ liệu của ML.

---

## Matplotlib

= nền tảng visualization.

---

## Seaborn

= visualization thống kê mạnh.

---

## EDA

= bước bắt buộc trước khi train model.

---

# 📌 23. Mục tiêu cuối cùng

Sau khi học xong chủ đề này cần có khả năng:

- Đọc dataset
- Hiểu dataset
- Cleaning dữ liệu
- Visualization dữ liệu
- Detect vấn đề dữ liệu
- Làm EDA thực tế
- Chuẩn bị dataset cho Machine Learning
- Debug dữ liệu trước khi train model

---

# 🚀 Final Conclusion

Nếu muốn đi theo:

- AI Engineer
- ML Engineer
- Data Scientist
- Data Analyst

thì:

## Pandas + NumPy + Visualization + EDA

là nền móng gần như bắt buộc phải cực kỳ vững trước khi học Machine Learning nâng cao.

