🩺 PHÂN LOẠI MỨC ĐỘ BÉO PHÌ DỰA TRÊN THÓI QUEN ĂN UỐNG & THỂ CHẤT
🎓 Institution: Khoa Công nghệ Thông tin - Đại học Nông Lâm TP.HCM 

🧑‍🤝‍🧑 Authors: * Phạm Đức Đại (21130304) * Võ Quốc Phong (21130474) 


📖 1. Giới thiệu (Introduction)
Béo phì đang là một trong những thách thức sức khỏe lớn nhất toàn cầu, dẫn đến nhiều nguy cơ như bệnh tim mạch hay tiểu đường. Dự án này được chúng tôi thực hiện với mục tiêu áp dụng sức mạnh của Học máy (Machine Learning) để giải quyết bài toán:

🎯 Mục tiêu: Phân loại mức độ béo phì của một cá nhân.

🔍 Cơ sở: Dựa trên dữ liệu về thói quen ăn uống và tình trạng thể chất.

🛡️ Ý nghĩa: Hỗ trợ tầm soát nguy cơ sớm và đưa ra các khuyến nghị y tế phù hợp.


🗂️ 2. Bộ Dữ Liệu (Dataset)
Chúng tôi sử dụng bộ dữ liệu "Estimation of obesity levels based on eating habits and physical condition" từ kho lưu trữ UCI Machine Learning Repository.

📦 Kích thước: 2111 mẫu dữ liệu.

🌎 Nguồn gốc: Mexico, Peru, và Colombia.

⚙️ Đặc trưng (16 Features): 

👤 Nhân khẩu học: Gender, Age, Height, Weight, Family history.

🍎 Thói quen ăn uống: FAVC (Đồ ăn giàu calo), FCVC (Rau củ), NCP (Số bữa chính), CAEC (Ăn vặt), CH2O (Uống nước), CALC (Rượu bia).

🏃 Lối sống & Vận động: SMOKE (Hút thuốc), SCC (Theo dõi calo), FAF (Tần suất vận động), TUE (Thời gian dùng thiết bị công nghệ), MTRANS (Phương tiện đi lại).

🏷️ Nhãn đầu ra (7 Mức độ): 

Thiếu cân (Insufficient Weight)

Bình thường (Normal Weight)

Thừa cân cấp độ I & II (Overweight Level I, II)

Béo phì loại I, II & III (Obesity Type I, II, III)

🛠️ 3. Phương Pháp Thực Hiện (Methodology)
Đây là bài toán Học có giám sát (Supervised Learning). Quy trình của chúng tôi bao gồm các bước chính:

🔄 Quy trình xử lý:

Tiền xử lý (Preprocessing): Kiểm tra lỗi, xử lý dữ liệu thiếu (Mean Imputer), và chuẩn hóa dữ liệu (MaxAbsScaler).


Chia dữ liệu: 80% Train - 20% Test.


Huấn luyện mô hình: Sử dụng 3 thuật toán phổ biến:

📉 Logistic Regression: Phân tích mối quan hệ tuyến tính.

📐 Support Vector Machine (SVM): Tìm siêu phẳng phân lớp tối ưu.

🌳 Random Forest: Kết hợp nhiều cây quyết định để xử lý dữ liệu phi tuyến.

🏆 4. Kết Quả Thực Nghiệm (Results)
Sau khi huấn luyện và kiểm thử, kết quả độ chính xác (Accuracy) của các mô hình như sau:

🥇 Rank	Model	Accuracy	Precision	Recall	F1 Score
🥇	Random Forest	95.27%	95.63%	95.27%	95.34%
🥈	SVM	74.47%	73.76%	74.47%	73.20%
🥉	Logistic Regression	69.74%	68.69%	69.74%	68.20%

Xuất sang Trang tính

💡 Nhận xét:


Random Forest hoạt động vượt trội nhất nhờ khả năng xử lý tốt các đặc trưng phi tuyến tính và giảm hiện tượng overfitting.


Logistic Regression cho kết quả thấp nhất, chứng tỏ dữ liệu có tính phức tạp cao mà mô hình tuyến tính khó nắm bắt.

🧩 5. Kết Luận (Conclusion)
Nghiên cứu của chúng tôi đã khẳng định:

✅ Random Forest là mô hình phù hợp nhất cho bài toán phân loại béo phì trên tập dữ liệu này.


🚀 Việc áp dụng AI vào y tế mang lại tiềm năng to lớn trong việc hỗ trợ ra quyết định và nâng cao chất lượng cuộc sống cộng đồng.

💻 6. Hướng Dẫn Cài Đặt (Installation)
Dự án được phát triển trên nền tảng Google Colab.

📂 Source Code: Phan_loai_muc_do_beo_phi.ipynb.

📚 Thư viện cần thiết:

numpy

pandas

scikit-learn
