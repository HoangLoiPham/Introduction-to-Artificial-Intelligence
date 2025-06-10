Câu 1 

1.1

![image](https://github.com/user-attachments/assets/78431465-5700-41c1-9bba-98ba4174a8a6)

gamma_correction: Phương pháp điều chỉnh độ sáng của ảnh dựa trên công thức gamma. Hàm này sử dụng một bảng (lookup table) để áp dụng công thức gamma:

invGamma = 1.0 / gamma: Tính giá trị nghịch đảo của gamma.

table = np.array([((i / 255.0) ** invGamma) * 255 for i in range(256)]): Tạo một bảng giá trị điều chỉnh theo gamma.

cv2.LUT(image, table): Áp dụng bảng điều chỉnh lên ảnh

1.2

![image](https://github.com/user-attachments/assets/3e6a1910-4854-47f7-b8de-fa7cd439a5f3)

log_transformation: Phương pháp này sử dụng phép toán logarit để tăng độ sáng cho các pixel có giá trị thấp.

c = 255 / np.log(1 + np.max(image)): Tính hệ số c để chuẩn hóa ảnh.

log_image = c * (np.log(image + 1)): Áp dụng phép toán logarit cho mỗi pixel của ảnh.

np.array(log_image, dtype=np.uint8): Đảm bảo rằng giá trị ảnh nằm trong phạm vi 0-255.

1.3

![image](https://github.com/user-attachments/assets/33e351b8-a6cd-46e4-8b30-1b213707f139)

histogram_equalization: Phương pháp cân bằng histrogram của ảnh để làm sáng hoặc tối các vùng trong ảnh.

cv2.cvtColor(image, cv2.COLOR_BGR2GRAY): Chuyển ảnh sang ảnh xám (grayscale) vì phương pháp cân bằng histogram chỉ áp dụng cho ảnh xám.

cv2.equalizeHist(gray_image): Thực hiện cân bằng histogram của ảnh xám

1.4  Kết quả 

![image](https://github.com/user-attachments/assets/a782a207-7d55-4b4f-b7e9-21f5e47d97ec)


Câu 2

2.1 

![image](https://github.com/user-attachments/assets/db13cf4e-26c7-4495-8cdf-89916d4428c5)

fast_fourier: Phương pháp này sử dụng biến đổi Fourier (FFT) để phân tích ảnh trong miền tần số.

cv2.cvtColor(image, cv2.COLOR_BGR2GRAY): Chuyển ảnh màu (BGR) thành ảnh xám (grayscale) vì biến đổi Fourier thường chỉ áp dụng cho ảnh xám.

cv2.dft(np.float32(gray_image), flags=cv2.DFT_COMPLEX_OUTPUT): Thực hiện biến đổi Fourier lên ảnh xám, sử dụng loại đầu ra phức (complex output).

np.fft.fftshift(dft): Dịch chuyển ảnh DFT để đưa thành phần tần số thấp về trung tâm.

cv2.magnitude(dft_shift[:, :, 0], dft_shift[:, :, 1]): Tính biên độ (magnitude) của tần số, để có thể hiển thị phổ tần số


2.2

![image](https://github.com/user-attachments/assets/25243388-7539-4879-a642-f152bcf8d5be)

butterworth_lowpass_filter: Bộ lọc Butterworth lọc bỏ các tần số cao, chỉ giữ lại tần số thấp.

dft_shift: Dịch chuyển DFT để các tần số thấp nằm ở trung tâm.

mask: Tạo một mặt nạ (mask) với giá trị giảm dần từ trung tâm ra ngoài. Các tần số thấp sẽ được giữ lại, trong khi các tần số cao sẽ bị giảm dần.

cv2.idft(fshift): Chuyển ảnh từ miền tần số trở lại miền không gian sau khi áp dụng bộ lọc

2.3

![image](https://github.com/user-attachments/assets/c814d5a8-4609-4416-855d-5efcd0c053dd)

butterworth_highpass_filter: Bộ lọc Butterworth lọc bỏ các tần số thấp, chỉ giữ lại các tần số cao.

mask: Mặt nạ ngược với bộ lọc thấp, nơi các tần số cao được giữ lại và tần số thấp bị loại bỏ

2.4 kết quả 

![image](https://github.com/user-attachments/assets/bca056e4-e1fb-419c-b69f-8a25ced57233)


Câu 3

3.1

![image](https://github.com/user-attachments/assets/40fea677-ddd1-4aae-8117-eeba8e19b247)

process_rgb_channels: Phương thức này xử lý ảnh RGB. Đầu tiên, ảnh được tách thành các kênh màu R, G, B. Sau đó, phương pháp xử lý sẽ được áp dụng cho từng kênh riêng biệt.

Tùy thuộc vào giá trị method_choice, các phép biến đổi như Image Inverse Transformation, Gamma Correction, Log Transformation, Histogram Equalization, và Contrast Stretching sẽ được áp dụng.

3.2 kết quả 

![image](https://github.com/user-attachments/assets/829c0420-584f-494c-9180-e48a76886e5d)

Câu 4

4.1 

![image](https://github.com/user-attachments/assets/ea626834-9401-45ee-9ebd-7be4a0024762)

log_transformation: Phương pháp sử dụng logarit để làm sáng các phần có giá trị pixel thấp trong ảnh.

np.clip(image, 1, 255): Đảm bảo rằng tất cả giá trị trong ảnh nằm trong khoảng từ 1 đến 255 để tránh lỗi log(0).

c = 255 / np.log(1 + np.max(image)): Tính giá trị hệ số c để chuẩn hóa ảnh.

log_image = c * (np.log(image + 1)): Áp dụng phép toán logarit lên ảnh và điều chỉnh giá trị pixel

4.2 

![image](https://github.com/user-attachments/assets/47c9919e-65e0-41b3-8142-b540a1c41da3)


histogram_equalization: Phương pháp cân bằng histogram của ảnh để làm tăng độ tương phản. Phương pháp này giúp làm sáng hoặc tối các vùng tối và sáng trong ảnh:

cv2.cvtColor(image, cv2.COLOR_BGR2GRAY): Chuyển ảnh màu sang ảnh xám (grayscale) vì histogram equalization chỉ áp dụng cho ảnh xám.

cv2.equalizeHist(gray_image): Áp dụng phương pháp cân bằng histogram trên ảnh xám

4.3 kết quả 

![image](https://github.com/user-attachments/assets/bed0c913-e427-42a3-9b53-b7f10441939b)













