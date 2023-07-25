# Bank Customer Churn Prediction

### Giới thiệu

Kho lưu trữ này chứa mã và tài liệu cho quy trình Xây dựng các mô hình dự báo khách hàng rời bỏ (Churn) trong ngân hàng. 
Mục tiêu của dự án này là tìm ra mô hình học máy phù hợp nhất để áp dụng cho dự báo khách hàng rời bỏ ngân hàng, giúp ngân hàng đưa ra những quyết định cần thiết để đối phó với điều đó.

### Nguồn dữ liệu và tổng quan

Bộ dữ liệu Churn_Modelling được lấy từ một chia sẻ trên kho dữ liệu Kaggle.
Nó bao gồm các thuộc tính của khách hàng, số liệu thống kê và các thông tin liên quan khác.

Bộ dữ liệu gốc của Churn_Modelling chứa 10.000 bản ghi dữ liệu khách hàng. Mỗi bản ghi đại diện cho một khách hàng duy nhất và bao gồm
các thuộc tính khác nhau như tên, tuổi, vị trí, số dư tài khoản, ước tính lương, v.v..


### Các công cụ được sử dụng

1. **Python**
2. **Pandas** cho **Data Manipulation**, **Cleaning**.
3. **Matplotlib, seabron** cho **Data Visualization**
4. **sci-kit learn** cho **Data Encoding**, xây dựng model, **Model Evaluation**

### Quy trình thực hiện

1. **Data Understanding** - Tập dữ liệu đã được kiểm tra kỹ lưỡng để hiểu cấu trúc, các cột và ý nghĩa của chúng.
   Dữ liệu không có từ điển dữ liệu kèm theo. Với sự trợ giúp của các nguồn trực tuyến, tôi đã có thể tạo một nguồn
   giúp tôi hiểu được ý nghĩa của tất cả các cột.
2. **Data Exploration** - Phân tích dữ liệu khám phá (**EDA**) đã được thực hiện để hiểu rõ hơn về dữ liệu, xác định các mẫu và phát hiện ra sự bất thường.
3. **Data Preprocessing**
- Thực hiện bỏ các cột không cần thiết cho quá trình dự báo (RowNumber, CustomerID, Surname).
- Thực hiện mã hóa các cột dữ liệu có dạng chữ thành số (Gender, Geography)
- Thực hiện xử lý Outliers với phương pháp **Capping** (CreditScore, Age)
- Thực hiện chuẩn hóa dữ liệu cho các biến độc lập với phương pháp **Min-Max Scaling**
- Xử lý mất cân bằng đối với biến mục tiêu bằng phương pháp Oversampling, cụ thể là kỹ thuật **SMOTE**
4. **Model Fitting** - Thực hiện xây dựng 5 mô hình dự báo áp dụng cho dự báo phân loại (classification): **Logistic Regression**, **Decision Tree**, **RandomForest**, **KNN và SVM**.
5. **Model Evaluation** - Thực hiện đánh giá, so sánh 5 mô hình dự báo, tìm ra mô hình tốt nhất bằng việc so sánh thông qua **accuracy score**, **classification report** và **ROC, AUC**.