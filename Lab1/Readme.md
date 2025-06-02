Nhập Môn xử lý ảnh số 

Lab 1 
  
  Câu 1 
  
  khai báo
  
  
  ![image](https://github.com/user-attachments/assets/6fe6fc8f-3c1d-4deb-9f80-d7cd2cf6486c)

  
  đọc file và hàm tách ảnh theo màu 
  
  
  ![image](https://github.com/user-attachments/assets/ad19e602-1c8a-4dfa-91aa-de801d783b74)

  hàm hiển thị kết quả ảnh 

  ![image](https://github.com/user-attachments/assets/b250fc14-92ae-4d90-aa87-641fbbb3e057)

  kết quả 

  ![image](https://github.com/user-attachments/assets/0494f732-00d4-4bfc-bbb2-f5894114fbdc)

  Câu 2

  hàm đọc hoán đổi kênh màu 

  ![image](https://github.com/user-attachments/assets/18b2036d-54bb-4887-bf50-44c1e50d9ad2)

  hàm hiển thị kết quả 

  ![image](https://github.com/user-attachments/assets/3f0a9edf-e9db-4052-b3c3-f134b0b86014)

  kết quả 

  ![image](https://github.com/user-attachments/assets/877f02bd-04ff-4bdb-bf7f-58265d148525)

  Câu 3

  hàm chuẩn hóa giá trị và chuyển đổi từng pixel sang HSV

  ![image](https://github.com/user-attachments/assets/ac252e95-fd0d-4580-a48c-03d19623c6bd)

 hàm lưu ảnh và show kết quả 
 
 ![image](https://github.com/user-attachments/assets/0be65773-2549-4baf-b4fe-1c7afbe92eb4)

 kết quả 

 ![image](https://github.com/user-attachments/assets/c4845245-b1e8-474b-9629-8ff6febd3238)

  Câu 4

  hàm chuyển RGB sang HSV

  ![image](https://github.com/user-attachments/assets/0557b1ea-6f2f-41b1-a51e-30e11591da35)

  hàm show kết quả 

  ![image](https://github.com/user-attachments/assets/41986c80-12d4-4813-bfcf-e0a90a410328)

  kết quả 

  ![image](https://github.com/user-attachments/assets/ec11826f-19f9-4af0-8e08-34b797404bb3)


Câu 5

hàm mean lọc trung bình 

![image](https://github.com/user-attachments/assets/a77b7cf4-9928-4329-9d73-79e852dc826e)

hàm hiển thị ảnh đã lộc

![image](https://github.com/user-attachments/assets/a3baa5c3-60fd-4b73-b269-61d25cd3810f)

kết quả 

![image](https://github.com/user-attachments/assets/3fcf31c6-c41d-4ab8-bdeb-18702eee2348)

Câu 6

hàm trả về 4 ảnh bằng 4 phương pháp khác nhau

![image](https://github.com/user-attachments/assets/7ea1dd4c-87d4-47b7-87bf-db1d81010c43)

hàm show kết quả và chuyển đổi BGR sang RGB

![image](https://github.com/user-attachments/assets/9d7aec32-1696-46a8-a5b3-473ce9bc3c44)

kết quả 
![image](https://github.com/user-attachments/assets/8ce576cc-a05d-4437-91a6-f614e4aa3b32)
![image](https://github.com/user-attachments/assets/896dd968-949b-4acb-b5ac-4ec164ef11ab)
![image](https://github.com/user-attachments/assets/fb9db193-912a-4602-9ccb-bdec6cdaea4e)

Câu 7 

7.1 Hàm denoise(img)

![image](https://github.com/user-attachments/assets/917b0f1f-7dd7-4a72-951a-7ccf2a1f3ba8)

Dùng lọc trung vị (median blur) với kernel size 5 để làm giảm nhiễu muối tiêu (salt-and-pepper noise) trên ảnh màu gốc.

Trả về ảnh đã được làm mượt (giảm nhiễu)

7.2 Hàm edge_detection(img_gray)

![image](https://github.com/user-attachments/assets/4ee18384-721c-4270-9ade-e92e26bedc60)

Input: Ảnh xám (grayscale) img_gray

Phát hiện cạnh bằng các phương pháp:

Canny: Phát hiện cạnh với ngưỡng 100 và 200.

Sobel:

Tính đạo hàm theo trục X (sobelx) và theo trục Y (sobely).

Tính biên độ cạnh tổng hợp (edges_sobel) bằng hàm magnitude của 2 đạo hàm.

Laplacian:

Tính đạo hàm bậc hai (Laplacian) để phát hiện cạnh, sau đó chuyển về dạng ảnh 8 bit.

Trả về 3 ảnh biên độ cạnh tương ứng.

7.3 VÒng lập xử lý nhiều ảnh 

![image](https://github.com/user-attachments/assets/d56f5c02-d0a1-4633-8eb4-5e3f4fc54807)

7.4 kết quả 

![image](https://github.com/user-attachments/assets/4572a97a-9a35-434c-9c73-0a1e80248351)
![image](https://github.com/user-attachments/assets/d5a7e62e-0242-4faf-85a8-3d26f468c027)
![image](https://github.com/user-attachments/assets/7f346229-e32f-42fd-ad7b-a628542920da)

Câu 8 

8.1 Hàm random_rgb_swap(img) 

![image](https://github.com/user-attachments/assets/d5cd9e7b-b615-4813-8442-ee1d9dcaddc2)

8.2 Vòng lặp xử lý ảnh:

![image](https://github.com/user-attachments/assets/67d57854-0508-4f2f-b08f-7da88d0e50de)

8.3 kết quả 
demo 1 ảnh 

![image](https://github.com/user-attachments/assets/07d29b0b-9b06-454b-9cbc-d7cdd620f186)

Câu 9 
 9.1 Hàm affine_transform(img, angle=30, tx=50, ty=30)

 ![image](https://github.com/user-attachments/assets/4df37aa4-2f71-465a-8ae6-d25426b1fcbe)

 img.shape[:2]: lấy kích thước ảnh (số hàng = chiều cao, số cột = chiều rộng).

cv2.getRotationMatrix2D(center, angle, scale):

Tạo ma trận biến đổi affine 2x3 để xoay ảnh quanh điểm center (ở đây là trung tâm ảnh: (cols/2, rows/2)).

angle: góc xoay (đơn vị độ, dương là xoay ngược chiều kim đồng hồ).

scale=1: giữ nguyên tỷ lệ (không phóng to/thu nhỏ).

9.2 Vòng lặp xử lý ảnh

![image](https://github.com/user-attachments/assets/42908bf5-cf26-4ec5-97a5-d3035303c7d3)

9.3 kết quả 
demo 1 ảnh 

![image](https://github.com/user-attachments/assets/3a6f5193-822a-48ad-be84-c0b73302f3a0)























  







