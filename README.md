Phân loại Mức độ Béo phì dựa trên Thói quen Ăn uống & Thể chất

Authors: Phạm Đức Đại & Võ Quốc Phong 


Institution: Khoa Công nghệ Thông tin - Đại học Nông Lâm TP.HCM 

 Giới thiệu (Introduction)
Béo phì là một vấn đề sức khỏe toàn cầu nghiêm trọng, liên quan mật thiết đến các bệnh lý tim mạch và đái tháo đường. Dự án này được chúng tôi thực hiện nhằm mục đích áp dụng các kỹ thuật Học máy (Machine Learning) để phân loại và dự đoán mức độ béo phì của một cá nhân dựa trên thói quen ăn uống và tình trạng thể chất của họ.



Mục tiêu chính là xây dựng một mô hình hỗ trợ tầm soát nguy cơ và đưa ra các khuyến nghị về sức khỏe.

 Dữ liệu (Dataset)
Chúng tôi sử dụng bộ dữ liệu "Estimation of obesity levels based on eating habits and physical condition" từ UCI Machine Learning Repository.


Kích thước: 2111 mẫu (từ Mexico, Peru, Colombia).




Đặc trưng (Features): 16 thuộc tính đầu vào bao gồm nhân khẩu học và thói quen sinh hoạt:


Nhân khẩu học: Gender, Age, Height, Weight, Family history.

Thói quen ăn uống: FAVC (Thức ăn giàu calo), FCVC (Rau củ), NCP (Số bữa ăn), CAEC (Ăn vặt), CH2O (Nước uống), CALC (Rượu bia).

Vận động: SMOKE, SCC (Theo dõi calo), FAF (Tần suất vận động), TUE (Dùng thiết bị công nghệ), MTRANS (Di chuyển).


Nhãn (Target): Phân loại thành 7 mức độ:

Insufficient Weight (Thiếu cân)

Normal Weight (Bình thường)

Overweight Level I & II

Obesity Type I, II & III

 Phương pháp & Kỹ thuật (Methodology)
Đây là bài toán phân loại thuộc nhóm Học có giám sát (Supervised Learning). Quy trình thực hiện của chúng tôi bao gồm:

Tiền xử lý dữ liệu (Preprocessing):

Kiểm tra và loại bỏ giá trị thiếu/không hợp lệ.

Chuẩn hóa dữ liệu (Normalization) để đồng nhất thang đo (sử dụng MaxAbsScaler).


Mã hóa các biến phân loại (Encoding).

Chia tập dữ liệu: 80% Training - 20% Testing.

Mô hình hóa (Modeling): Chúng tôi đã thử nghiệm và so sánh 3 thuật toán:


Logistic Regression: Phân tích mối quan hệ tuyến tính.


Support Vector Machine (SVM): Tìm siêu phẳng tối ưu để phân tách các lớp dữ liệu.



Random Forest: Sử dụng tập hợp các cây quyết định để xử lý dữ liệu phi tuyến tính và giảm overfitting.


 Kết quả Thực nghiệm (Results)
Sau khi huấn luyện và đánh giá trên tập kiểm tra, kết quả thu được như sau:

Model	Accuracy	Precision	Recall	F1 Score
Logistic Regression	69.74%	68.69%	69.74%	68.20%
SVM	74.47%	73.76%	74.47%	73.20%
Random Forest	95.27%	95.63%	95.27%	95.34%

Xuất sang Trang tính

Nhận xét:


Logistic Regression cho kết quả thấp nhất do hạn chế trong việc nắm bắt các mối quan hệ phức tạp, phi tuyến tính của bộ dữ liệu.


Random Forest là mô hình hiệu quả nhất với độ chính xác vượt trội (~95%), chứng tỏ khả năng xử lý tốt đa cộng tuyến và dữ liệu phức tạp.


 Hướng dẫn chạy (How to run)
Dự án được triển khai trên môi trường Google Colab.


Source code: Phan_loai_muc_do_beo_phi.ipynb.

Thư viện yêu cầu: Python, Scikit-learn, Pandas, NumPy.
