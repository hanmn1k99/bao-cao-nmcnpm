# 📘 MINI APP ĐẶT BÀN NHÀ HÀNG  
## Báo cáo nội dung slide – Nhập Môn Công Nghệ Phần Mềm

---

# 1. Giới thiệu nhóm
**Nhóm thực hiện:**  
- **Nguyễn Sơn** – Backend (Quản lý bàn)  
- **Vũ Anh** – Backend (Quản lý đặt bàn)  
- **Trần Nghĩa** – UI/UX  
- **Minh** – Testing (JUnit, Postman, Selenium)  
- **Nguyễn Minh Hân** – Báo cáo, slide, UI hỗ trợ  

---

# 2. Mục tiêu và phạm vi đề tài

## 🎯 Mục tiêu
- Xây dựng ứng dụng đặt bàn đơn giản, rõ ràng, tối ưu thao tác cho nhân viên nhà hàng.
- Ứng dụng quy trình phát triển phần mềm: Agile–Scrum.
- Tích hợp kiểm thử tự động và CI/CD.

## 📌 Phạm vi
- Chức năng quản lý bàn.
- Chức năng quản lý đặt bàn.
- Chức năng thanh toán.
- Giao diện demo (UI MVP).
- Backend Spring Boot, database H2/MySQL.
- Kiểm thử: JUnit, Postman, Selenium.

---

# 3. Vấn đề & Insight người dùng

## ❗ Vấn đề thực tế
- Ghi chép thủ công gây nhầm lẫn, trùng lịch.
- Khó theo dõi trạng thái bàn theo thời gian thực.
- Xử lý đặt – hủy – chuyển bàn tốn thời gian.

## 💡 Insight người dùng
- Cần nhìn rõ trạng thái từng bàn: *trống / đã đặt / đang dùng*.
- Cần thao tác nhanh, chính xác.
- Giao diện đơn giản, tránh quá nhiều thao tác.

---

# 4. Kiến trúc & Công nghệ

## 🧩 Kiến trúc hệ thống đề xuất
- Client → REST API (Spring Boot) → Service → Database (H2/MySQL)
- Testing layer:
  - Unit test (JUnit)
  - API test (Postman / MockMVC)
  - UI test (Selenium)

## 🛠 Công nghệ
- **Backend:** Spring Boot  
- **Database:** H2 / MySQL  
- **Testing:** JUnit, Mockito, Postman, Selenium  
- **DevOps:** GitHub, GitHub Actions / Jenkins  
- **IDE:** Visual Studio Code  

---

# 5. Phân công thành viên (CLO1)

| Thành viên | Phụ trách |
|-----------|-----------|
| **Nguyễn Sơn** | API quản lý bàn, Unit Test |
| **Vũ Anh** | API đặt bàn, xử lý thanh toán |
| **Trần Nghĩa** | Thiết kế UI/UX, wireframe |
| **Minh** | JUnit, Selenium, Postman, báo cáo test |
| **Nguyễn Minh Hân** | Báo cáo, slide, UI demo, tổng hợp |

---

# 6. Yêu cầu chức năng (Functional Requirements)

## 📌 Quản lý bàn
- Thêm bàn
- Cập nhật bàn
- Xóa bàn
- Tìm kiếm bàn
- Hiển thị trạng thái bàn

## 📌 Quản lý đặt bàn
- Tạo đặt bàn
- Cập nhật thông tin
- Hủy đặt bàn
- Xử lý thanh toán

## 📌 Giao diện người dùng
- Trang chủ
- Danh sách bàn
- Lịch đặt bàn
- Thông báo (nếu có)

---

# 7. UI/UX – Định hướng thiết kế

## 🎨 Mục tiêu UI
- Tối giản, thao tác nhanh.
- Ưu tiên khả năng quan sát trạng thái bàn.
- Giao diện rõ ràng, dễ dùng.

## 🌈 Quy ước màu sắc gợi ý
- **Xanh:** Bàn trống  
- **Vàng:** Bàn đã đặt  
- **Đỏ:** Bàn đang dùng  

## 📱 Wireframe đề xuất
- Màn hình Home
- Màn hình Danh sách bàn (dạng grid)
- Form đặt bàn
- Màn hình thanh toán

---

# 8. Demo giao diện (Wireframe / UI)
*(Thêm ảnh hoặc Figma link vào đây)*

---

# 9. Chiến lược kiểm thử (Testing Strategy – CLO2)

## ✅ Unit Test – JUnit
- Test nghiệp vụ: createBooking(), updateTable(), validate input.
- Mock service bằng Mockito.

## ✅ API Test – Postman / MockMVC
- Test các endpoint:
  - POST /tables
  - POST /bookings
  - PUT /bookings/{id}
  - DELETE /bookings/{id}
- Kiểm tra status code, schema, validation.

## ✅ UI Test – Selenium
- Kịch bản test:
  - Mở trang → chọn bàn → đặt bàn → lưu → hiển thị kết quả.

---

# 10. Kết quả kiểm thử

## 📊 Test Case
- TC01: Tạo bàn mới – PASS  
- TC02: Đặt bàn thiếu tên khách – FAIL (đã fix)  
- TC03: Hủy đặt bàn – PASS  
- TC04: Selenium test UI – PASS  

## 📈 Tỷ lệ bao phủ (coverage)
*(Điền sau khi Minh thống kê)*

---

# 11. Quy trình Agile – Scrum

## 🌀 Sprint 1  
- Phân tích yêu cầu  
- Use case  
- ERD  
- Wireframe UI  

## 🌀 Sprint 2  
- API quản lý bàn  
- API đặt bàn  
- Unit Test  

## 🌀 Sprint 3  
- Xây dựng UI demo  
- API test  
- UI test  

## 📝 Daily Scrum  
- Việc đã làm – việc sẽ làm – khó khăn  

## ✅ Review & Retrospective  
- Nhận xét tiến độ  
- Cải thiện workflow

---

# 12. CI/CD – GitHub Actions

## 🚀 Quy trình tự động
1. Push code → GitHub Actions build  
2. Chạy JUnit  
3. Báo kết quả  
4. PR → Review → Merge  

## ✅ Lợi ích
- Giảm lỗi build thủ công  
- Tiết kiệm thời gian  
- Đảm bảo chất lượng trước khi merge  

---

# 13. Kết quả đạt được
- Hoàn thiện API Spring Boot cho các chức năng chính.  
- Tạo được UI demo rõ ràng.  
- Áp dụng đầy đủ bộ kiểm thử JUnit – Postman – Selenium.  
- Quy trình nhóm tuân thủ Agile – Scrum.  
- Triển khai CI/CD tự động bằng GitHub Actions.

---

# 14. Hạn chế
- Chưa có phân quyền đăng nhập.  
- Chưa hỗ trợ realtime trạng thái bàn.  
- Giao diện ở mức demo, chưa tối ưu trải nghiệm.  
- Chưa có tính năng thông báo.

---

# 15. Hướng phát triển
- Gợi ý bàn trống tự động theo khung giờ.  
- WebSocket để cập nhật realtime.  
- Ứng dụng mobile bằng React Native.  
- Thêm thống kê doanh thu – báo cáo hiệu suất.  
- Triển khai hệ thống lên cloud để sử dụng thực tế.

---

# 16. Demo & Tài nguyên dự án
- **GitHub Repository:** …  
- **Video Demo:** …  
- **Tài liệu báo cáo:** …  

---

# 17. Q&A
Sẵn sàng trả lời câu hỏi.