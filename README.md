<h2 align="center">
    <a href="https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin">
    🎓 Faculty of Information Technology (DaiNam University)
    </a>
</h2>
<h2 align="center">
 ỨNG DỤNG DỰ BÁO THỚI TIẾT ONLINE
</h2>
<div align="center">
    <p align="center">
        <img src="docs/aiotlab_logo.png" alt="AIoTLab Logo" width="170"/>
        <img src="docs/fitdnu_logo.png" alt="FITDNU Logo" width="180"/>
        <img src="docs/dnu_logo.png" alt="DaiNam University Logo" width="200"/>
    </p>

[![AIoTLab](https://img.shields.io/badge/AIoTLab-green?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Faculty of Information Technology](https://img.shields.io/badge/Faculty%20of%20Information%20Technology-blue?style=for-the-badge)](https://dainam.edu.vn/vi/khoa-cong-nghe-thong-tin)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-orange?style=for-the-badge)](https://dainam.edu.vn)

</div>

# 🌐 1. Giới thiệu hệ thống
Đây là đồ án môn học **Lập trình mạng** với yêu cầu **xây dựng ứng dụng dự báo thời tiết trực tuyến sử dụng giao thức UDP**.  
Ứng dụng cho phép **nhiều client đồng thời** gửi yêu cầu tới server để lấy thông tin thời tiết từ API **OpenWeatherMap** và hiển thị trong giao diện **Java Swing**.

---

# 🛠 2. Công nghệ sử dụng
- **Ngôn ngữ:** Java (JDK 11+)  
- **Giao thức:** UDP (User Datagram Protocol)  
- **Giao diện:** Java Swing  
- **API:** [OpenWeatherMap](https://openweathermap.org/api)  
- **Quản lý lịch sử:** File `history.txt` (HistoryManager.java)  

---

# 📊 3. Hình ảnh & chức năng

## 🔑 Chức năng chính
- [x] Dự báo thời tiết hiện tại (nhiệt độ, mô tả, icon).  
- [x] Biểu đồ dự báo trung bình nhiệt độ 5 ngày.  
- [x] Lưu lịch sử truy vấn (ngày giờ, thành phố, loại yêu cầu).  
- [x] Hỗ trợ nhiều client đồng thời.  
- [x] Giao diện đồ họa (GUI) thân thiện bằng **Java Swing**.  

## 🖼 Hình ảnh minh họa giao diện
- Ô nhập thành phố + nút thao tác.  
- TextArea hiển thị kết quả.  
- Icon thời tiết (từ OpenWeather).  
- Biểu đồ dự báo 5 ngày.  

<img width="586" height="410" alt="image" src="https://github.com/user-attachments/assets/0cbab42c-452f-40f1-bd10-14773d4d8346" />
<img width="586" height="410" alt="image" src="https://github.com/user-attachments/assets/e2e9b26c-7cef-445d-966f-b232577c8f20" />

---

# 🚀 4. Hướng dẫn sử dụng và cài đặt

## Yêu cầu
- Cài đặt **Java JDK 11+** (có hỗ trợ module `java.desktop`).  
- Có kết nối Internet để gọi OpenWeather API.  
- Đăng ký **API key** từ [OpenWeatherMap](https://openweathermap.org/api).  

## Các bước cài đặt
1. **Clone hoặc tải source code** về máy.  
2. Mở file `WeatherServerMulti.java` và thay API key:
   ```java
   private static final String API_KEY = "YOUR_API_KEY";
3.Biên dịch code:
javac --add-modules java.desktop *.java
4.Chạy server:
java --add-modules java.desktop WeatherServerMulti
5.Chạy client (có thể mở nhiều client cùng lúc):
java --add-modules java.desktop WeatherClientGUIFull
💡 Ý tưởng phát triển thêm

Hỗ trợ đa ngôn ngữ (tiếng Việt, tiếng Anh).

Hiển thị nhiều thông tin hơn (độ ẩm, tốc độ gió, áp suất).

Lưu lịch sử vào cơ sở dữ liệu thay vì file.

Cảnh báo thời tiết (mưa, bão).

Phát triển ứng dụng mobile (Android/iOS) kết nối tới server UDP.
