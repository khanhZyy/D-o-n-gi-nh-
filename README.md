# Dataset House Price Prediction
Tập dữ liệu mô tả giá 
của các căn chung cư gồm 24949 dòng với 16 cột: 
• DiaChi: Mô tả địa chỉ của chung cư.  
• TinhTrangBDS: Mô tả tình trạng của chung cư (Đã bàn giao hoặc chưa bàn giao cho khách)  
• DienTich: Mô tả diện tích của chung cư.  
• Gia/m2: Mô tả giá của 1 mét vuông.   
• Phongngu: Mô tả số lượng phòng ngủ.   
• TenPhanKhu: Mô tả block của căn chung cư.   
• SoTang: Mô tả chung cư nằm ở tầng bao nhiêu.   
• PhongTam: Số lượng nhà vệ sinh.  
• Loai: Mô tả loại hình chung cư (Chung cư, căn hộ dịch vụ, penthouse, duxlex, tập thể, officetel).  
• GiayTo: tình trạng pháp lý của căn nhà (đã có số, đang chờ sổ, giấy tờ khác).  
• MaCanHo: mã căn hộ.  
• TinhTrangNoiThat: nội thất cao cấp, nội thất đầy đủ, nhà thô, hoàn thiện cơ bản.  
• HuongCuaChinh: hướng cửa chính của chung cư.  
• HuongBanCong: hướng ban công của chung cư.  
• DacDiem: căn trong góc hoặc căn chính giữa.  
• Gia: giá bán của căn hộ.  

# Thực hiện bài toán
Sơ đồ thực hiện bài toán
![image](https://github.com/user-attachments/assets/61d5b3d1-aa36-44ba-a19c-1f8609a27e23)

Kết quả sau khi huấn luyện
![image](https://github.com/user-attachments/assets/cb9011ac-4613-4100-a267-daf2982a4231)

Xây dựng 2 mô hình Random Forest Regressor (RFR) và Support Vector Regression (SVR)
Trong bài toán này, tôi sử dụng phương pháp RandomizedSearchCV để xác định các siêu tham số phù hợp cho hai mô hình SVR và RFR. RandomizedSearchCV thực hiện tìm kiếm ngẫu nhiên các tổ hợp siêu tham số từ các lưới tham số đã định nghĩa và đánh giá mô hình trên tập dữ liệu sử dụng phương pháp cross-validation. RandomizedSearchCV được chọn thay vì GridSearchCV, do nó hiệu quả hơn về mặt thời gian khi làm việc với không gian tham số lớn, đồng thời vẫn cung cấp kết quả tối ưu gần như tương đương.  
Kết quả cho thấy Random Forest Regressor (RFR) vượt trội hơn Support Vector Regression (SVR) ở hầu hết các chỉ số đánh giá. Cụ thể, RFR có các giá trị MAE, MSE và RMSE thấp hơn, đồng nghĩa với việc có độ chính xác cao hơn và ít lỗi hơn trong dự đoán. Bên cạnh đó, giá trị R² và R² hiệu chỉnh của RFR cũng cao hơn, cho thấy khả năng giải thích biến thiên của dữ liệu tốt hơn. Mặc dù RFR có thời gian thực thi dài hơn so với SVR, tuy nhiên, sự chênh lệch này là không đáng kể so với lợi ích mà RFR mang lại về mặt độ chính xác và khả năng giải thích. Nhìn chung, mô hình RFR là lựa chọn tốt hơn cho bài toán dự đoán giá nhà 
trong trường hợp này. 



