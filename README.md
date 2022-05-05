# DỰ BÁO NHIỆT ĐỘ PHÒNG SỬ DỤNG CẢM BIẾN NHIỆT ĐỘ VÀ TRÍ TUỆ NHÂN TẠO
### Tổng quan : Trong các yếu tố tác động trực tiếp đến con người của môi trường không khí, nhiệt độ là yếu tố quan trọng tác động đến sức khỏe và quá trình hoạt động khác của con người. Cuộc sống của con người sẽ không được đảm bảo nếu nhiệt độ ở mức quá cao hoặc quá thấp. Sự cần thiết của việc biết trước dữ liệu về môi trường sống của chúng ta trong tương lai thông qua các cảm biến thông thường, có thể giúp con người cải thiện được môi trường sống một cách trong lành và giảm được các rủi ro về sức khỏe.
#### I.Sơ đồ tổng quan của hệ thống
  + Về phần cứng : Sử dụng Kit Wemos D1 kết nối với cảm biển nhiệt độ để đọc dữ liệu rồi thông qua kết nối Wifi để cập nhật dữ liệu lên Google Sheets
  + Về cập nhật dữ liệu:Ta sẽ sử dụng tiện ích Google sheet có sẵn trong Google Driver kết hợp cùng với Google Apps Script tạo một API  để cập nhật dữ liệu từ Wemos D1 thông qua kết nối Wifi lên Google Sheets
  + Về xử lý và huấn luyện dữ liệu: Ta sử dụng Google Colab để xử lý tính toán dữ liệu và áp dụng mô hình LSTM để huấn luyện dữ liệu nhằm mục dự đoán nhiệt độ
  + ![image](https://user-images.githubusercontent.com/92384494/166856483-791d60cd-aacb-49e0-b979-f25e1bd12227.png)
#### II.Thu Thập dữ liệu nhiệt độ và cập nhật lên Google Sheet
  + Tham khảo video : https://www.youtube.com/watch?v=okNECYf2xlY
  + Code : https://drive.google.com/file/d/1I2C_W4aw6gnJR27QAEaQBddxFssY8Ls-/view
  + Tập dữ liệu sau khi thu thập : LM35_TEST.csv
  + ![image](https://user-images.githubusercontent.com/92384494/166856929-f16c2f78-ae0a-4887-b13a-824a4ba7daeb.png)
  + ![image](https://user-images.githubusercontent.com/92384494/166857003-22668ce1-464f-49eb-a96d-dd4584d1f488.png)
#### III.Tiến hành sử lý dữ liệu và huấn luyện mô hình sủ dụng mạng LSTM
  + Tham khảo về mô hình mạng RNN và LSTM : https://dominhhai.github.io/vi/2017/10/what-is-rnn/
  + Link Google Colab : https://colab.research.google.com/drive/1AHkA-7tSUBN9doDijVK2BFVIRwuCPXyF
  + File code : LSTM.ipynb
  + ![image](https://user-images.githubusercontent.com/92384494/166881645-c35aebe2-cb6e-431a-b4df-e4959161174c.png)
  + ![image](https://user-images.githubusercontent.com/92384494/166881685-35f1db94-0876-4de9-924d-70de3b94f7d0.png)
#### V. Dự đoán kết quả
  + Sử dụng file trọng số sau quá trình huấn luyện để tiến hành dự đoán
  + File trọng số đã train sẵn : 10_7.h5
  + ![image](https://user-images.githubusercontent.com/92384494/166857130-3ef36f74-6568-44d9-966a-268808a90b7f.png)
  + ![image](https://user-images.githubusercontent.com/92384494/166857141-77b40f59-2e26-403a-9ac0-20e9b4616157.png)

