# 🥗 **PHÂN LOẠI MỨC ĐỘ BÉO PHÌ DỰA TRÊN THÓI QUEN ĂN UỐNG & THỂ CHẤT**

> 🏛️ **Institution:** Khoa Công nghệ Thông tin - Đại học Nông Lâm TP.HCM
>
> 👥 **Authors:**
> **Phạm Đức Đại** (21130304) [cite: 3]
> **Võ Quốc Phong** (21130474) [cite: 4]

---
---

## 📖 **1. GIỚI THIỆU (INTRODUCTION)**

Béo phì đang là một trong những thách thức sức khỏe lớn nhất toàn cầu, dẫn đến nhiều nguy cơ nghiêm trọng như bệnh tim mạch, đái tháo đường và ung thư[cite: 15]. [cite_start]Dự án này được chúng tôi thực hiện nhằm mục đích áp dụng các kỹ thuật **Học máy (Machine Learning)** để giải quyết bài toán phân loại sức khỏe dựa trên dữ liệu thực tế[cite: 8].

* 🎯 **Mục tiêu:** Phân loại mức độ béo phì của một cá nhân[cite: 8].
* 🔍 **Đầu vào:** Dựa trên dữ liệu về thói quen ăn uống và tình trạng thể chất[cite: 16].
* 🛡️ **Ý nghĩa:** Hỗ trợ tầm soát nguy cơ sớm, cá nhân hóa trị liệu và giúp đưa ra các quyết định y tế thông minh hơn[cite: 19, 20, 21].

---

## 🗂️ **2. BỘ DỮ LIỆU (DATASET)**

Chúng tôi sử dụng bộ dữ liệu **"Estimation of obesity levels based on eating habits and physical condition"** từ kho lưu trữ **UCI Machine Learning Repository**[cite: 22].

* 📦 **Kích thước:** 2111 mẫu dữ liệu[cite: 10].
* 🌎 **Nguồn gốc:** Mexico, Peru, và Colombia[cite: 152].
* ⚙️ **Đặc trưng (16 Features):** Bộ dữ liệu bao gồm 16 thuộc tính quan trọng[cite: 10, 152]:

    * 👤 **Nhân khẩu học:** Gender (Giới tính), Age (Tuổi), Height (Chiều cao), Weight (Cân nặng), Family history (Tiền sử gia đình)[cite: 163, 164, 165, 166, 167].
    * 🍔 **Thói quen ăn uống:**
        * `FAVC`: Tiêu thụ thực phẩm giàu calo[cite: 168].
        * `FCVC`: Tần suất ăn rau củ[cite: 169].
        * `NCP`: Số bữa ăn chính[cite: 170].
        * `CAEC`: Ăn vặt giữa giờ[cite: 171].
        * `CH2O`: Lượng nước uống hàng ngày[cite: 173].
        * `CALC`: Tiêu thụ rượu bia[cite: 178].
    * 🏃 **Lối sống & Vận động:**
        * `SMOKE`: Hút thuốc[cite: 172].
        * `SCC`: Theo dõi lượng calo[cite: 175].
        * `FAF`: Tần suất hoạt động thể chất[cite: 176].
        * `TUE`: Thời gian dùng thiết bị công nghệ[cite: 177].
        * `MTRANS`: Phương tiện di chuyển[cite: 179].

🏷️ **Nhãn đầu ra (7 Mức độ):**
Từ *Thiếu cân*, *Bình thường*, *Thừa cân (Cấp I, II)* đến *Béo phì (Loại I, II, III)*[cite: 62].

---

## 🛠️ **3. PHƯƠNG PHÁP THỰC HIỆN (METHODOLOGY)**

Đây là bài toán **Phân loại (Classification)** thuộc nhóm Học có giám sát[cite: 60]. Quy trình thực hiện của nhóm như sau:

### 🔄 **Quy trình xử lý:**
1.  **Tiền xử lý (Preprocessing):**
    * Kiểm tra và loại bỏ dữ liệu lỗi/thiếu[cite: 156].
    * Chuẩn hóa dữ liệu để đồng nhất thang đo (Normalization)[cite: 157].
    * Mã hóa các thuộc tính phân loại sang dạng số[cite: 158].
2. **Chia dữ liệu:** Tập Train (80%) - Tập Test (20%)[cite: 160].
3.  **Mô hình hóa:** Chúng tôi triển khai và so sánh 3 thuật toán[cite: 9]:
    * 📉 **Logistic Regression:** Phân tích mối quan hệ tuyến tính[cite: 23].
    * 📐 **Support Vector Machine (SVM):** Tìm siêu phẳng phân tách tối ưu[cite: 25, 28].
    * 🌳 **Random Forest:** Kết hợp nhiều cây quyết định (Decision Trees) để xử lý dữ liệu phi tuyến tính và tránh overfitting[cite: 24].

---

## 🏆 **4. KẾT QUẢ THỰC NGHIỆM (RESULTS)**

Sau khi huấn luyện và đánh giá trên tập kiểm tra, kết quả độ chính xác (Accuracy) của các mô hình như sau[cite: 185]:

| 🥇 Rank | Model | Accuracy | Precision | Recall | F1 Score |
| :---: | :--- | :---: | :---: | :---: | :---: |
| 🥇 | **Random Forest** | **95.27%** | **95.63%** | **95.27%** | **95.34%** |
| 🥈 | **SVM** | 74.47% | 73.76% | 74.47% | 73.20% |
| 🥉 | **Logistic Regression** | 69.74% | 68.69% | 69.74% | 68.20% |

💡 **Nhận xét:**
* **Random Forest** hoạt động vượt trội nhất (~95%) nhờ khả năng xử lý tốt các đặc trưng phi tuyến tính và giảm hiện tượng overfitting[cite: 13, 188].
* **Logistic Regression** cho kết quả thấp nhất (~69%), cho thấy dữ liệu có tính phức tạp cao mà mô hình tuyến tính không thể nắm bắt hết[cite: 187].

---

## 🧩 **5. KẾT LUẬN (CONCLUSION)**

Qua quá trình nghiên cứu, chúng tôi rút ra các kết luận sau:
1.  ✅ **Random Forest** là mô hình phù hợp nhất cho bài toán phân loại béo phì trên tập dữ liệu này[cite: 196].
2.  🚀 Việc lựa chọn đúng mô hình học máy (dựa trên đặc thù dữ liệu) đóng vai trò quyết định đến hiệu suất dự đoán[cite: 197].
3.  🏥 Kết quả này mở ra tiềm năng ứng dụng AI trong y tế, giúp cảnh báo sớm và nâng cao chất lượng cuộc sống[cite: 198].

---

## 💻 **6. HƯỚNG DẪN CÀI ĐẶT (INSTALLATION)**

Dự án được phát triển trên nền tảng **Google Colab**.

* 📂 **Source Code:** `Phan_loai_muc_do_beo_phi.ipynb`.
* 📚 **Thư viện cần thiết:**
    * `numpy`
    * `pandas`
    * `scikit-learn`

---
