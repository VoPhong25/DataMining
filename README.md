# 🥗 **PHÂN LOẠI MỨC ĐỘ BÉO PHÌ DỰA TRÊN THÓI QUEN ĂN UỐNG & THỂ CHẤT**

> 🏛️ **Institution:** Khoa Công nghệ Thông tin - Đại học Nông Lâm TP.HCM
>
> 👥 **Authors:**
> **Phạm Đức Đại** (21130304) 
> **Võ Quốc Phong** (21130474) 

---
---

## 📖 **1. GIỚI THIỆU (INTRODUCTION)**

Béo phì đang là một trong những thách thức sức khỏe lớn nhất toàn cầu, dẫn đến nhiều nguy cơ nghiêm trọng như bệnh tim mạch, đái tháo đường và ung thư. Dự án này được chúng tôi thực hiện nhằm mục đích áp dụng các kỹ thuật **Học máy (Machine Learning)** để giải quyết bài toán phân loại sức khỏe dựa trên dữ liệu thực tế.

* 🎯 **Mục tiêu:** Phân loại mức độ béo phì của một cá nhân.
* 🔍 **Đầu vào:** Dựa trên dữ liệu về thói quen ăn uống và tình trạng thể chất.
* 🛡️ **Ý nghĩa:** Hỗ trợ tầm soát nguy cơ sớm, cá nhân hóa trị liệu và giúp đưa ra các quyết định y tế thông minh hơn.

---

## 🗂️ **2. BỘ DỮ LIỆU (DATASET)**

Chúng tôi sử dụng bộ dữ liệu **"Estimation of obesity levels based on eating habits and physical condition"** từ kho lưu trữ **UCI Machine Learning Repository**.

* 📦 **Kích thước:** 2111 mẫu dữ liệu.
* 🌎 **Nguồn gốc:** Mexico, Peru, và Colombia.
* ⚙️ **Đặc trưng (16 Features):** Bộ dữ liệu bao gồm 16 thuộc tính quan trọng:

    * 👤 **Nhân khẩu học:** Gender (Giới tính), Age (Tuổi), Height (Chiều cao), Weight (Cân nặng), Family history (Tiền sử gia đình).
    * 🍔 **Thói quen ăn uống:**
        * `FAVC`: Tiêu thụ thực phẩm giàu calo.
        * `FCVC`: Tần suất ăn rau củ.
        * `NCP`: Số bữa ăn chính.
        * `CAEC`: Ăn vặt giữa giờ.
        * `CH2O`: Lượng nước uống hàng ngày.
        * `CALC`: Tiêu thụ rượu bia.
    * 🏃 **Lối sống & Vận động:**
        * `SMOKE`: Hút thuốc.
        * `SCC`: Theo dõi lượng calo.
        * `FAF`: Tần suất hoạt động thể chất.
        * `TUE`: Thời gian dùng thiết bị công nghệ.
        * `MTRANS`: Phương tiện di chuyển.

🏷️ **Nhãn đầu ra (7 Mức độ):**
Từ *Thiếu cân*, *Bình thường*, *Thừa cân (Cấp I, II)* đến *Béo phì (Loại I, II, III)*.

---

## 🛠️ **3. PHƯƠNG PHÁP THỰC HIỆN (METHODOLOGY)**

Đây là bài toán **Phân loại (Classification)** thuộc nhóm Học có giám sát[cite: 60]. Quy trình thực hiện của nhóm như sau:

### 🔄 **Quy trình xử lý:**
1.  **Tiền xử lý (Preprocessing):**
    * Kiểm tra và loại bỏ dữ liệu lỗi/thiếu.
    * Chuẩn hóa dữ liệu để đồng nhất thang đo (Normalization).
    * Mã hóa các thuộc tính phân loại sang dạng số.
2. **Chia dữ liệu:** Tập Train (80%) - Tập Test (20%).
3.  **Mô hình hóa:** Chúng tôi triển khai và so sánh 3 thuật toán:
    * 📉 **Logistic Regression:** Phân tích mối quan hệ tuyến tính.
    * 📐 **Support Vector Machine (SVM):** Tìm siêu phẳng phân tách tối ưu.
    * 🌳 **Random Forest:** Kết hợp nhiều cây quyết định (Decision Trees) để xử lý dữ liệu phi tuyến tính và tránh overfitting.

---

## 🏆 **4. KẾT QUẢ THỰC NGHIỆM (RESULTS)**

Sau khi huấn luyện và đánh giá trên tập kiểm tra, kết quả độ chính xác (Accuracy) của các mô hình như sau:

| 🥇 Rank | Model | Accuracy | Precision | Recall | F1 Score |
| :---: | :--- | :---: | :---: | :---: | :---: |
| 🥇 | **Random Forest** | **95.27%** | **95.63%** | **95.27%** | **95.34%** |
| 🥈 | **SVM** | 74.47% | 73.76% | 74.47% | 73.20% |
| 🥉 | **Logistic Regression** | 69.74% | 68.69% | 69.74% | 68.20% |

💡 **Nhận xét:**
* **Random Forest** hoạt động vượt trội nhất (~95%) nhờ khả năng xử lý tốt các đặc trưng phi tuyến tính và giảm hiện tượng overfitting.
* **Logistic Regression** cho kết quả thấp nhất (~69%), cho thấy dữ liệu có tính phức tạp cao mà mô hình tuyến tính không thể nắm bắt hết.

---

## 🧩 **5. KẾT LUẬN (CONCLUSION)**

Qua quá trình nghiên cứu, chúng tôi rút ra các kết luận sau:
1.  ✅ **Random Forest** là mô hình phù hợp nhất cho bài toán phân loại béo phì trên tập dữ liệu này.
2.  🚀 Việc lựa chọn đúng mô hình học máy (dựa trên đặc thù dữ liệu) đóng vai trò quyết định đến hiệu suất dự đoán.
3.  🏥 Kết quả này mở ra tiềm năng ứng dụng AI trong y tế, giúp cảnh báo sớm và nâng cao chất lượng cuộc sống.

---

## 💻 **6. HƯỚNG DẪN CÀI ĐẶT (INSTALLATION)**

Dự án được phát triển trên nền tảng **Google Colab**.

* 📂 **Source Code:** [Bấm vào đây để mở Google Colab](https://colab.research.google.com/drive/1zDMmn_w5vRAgycphbwAK2lSlEmEJE1Vf?usp=sharing)
* 📚 **Thư viện cần thiết:**
    * `numpy`
    * `pandas`
    * `scikit-learn`

---
