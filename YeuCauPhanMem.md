## Chức năng chính của hệ thống:

Nhập dữ liệu giao dịch: Tải lên tệp sao kê ngân hàng (CSV, Excel, PDF).
Phân tích giao dịch: Tính toán thống kê giao dịch, phân loại theo các tiêu chí.
Lưu trữ kết quả phân tích: Lưu kết quả vào cơ sở dữ liệu.
## Tác nhân liên quan:

Người dùng: Tải lên tệp sao kê, xem kết quả phân tích, yêu cầu báo cáo.
Hệ thống phân tích: Xử lý và phân tích dữ liệu giao dịch.
Biểu đồ ca sử dụng
## Biểu dồ hệ thống
![Diagram](https://www.planttext.com/plantuml/png/HCmn2i8m583X_PtYuUuLfBeLH0LxWKSQsj0qrUG55N5sy1Ow5vtReOFWFN82ho3fulGl7_-t7nB7PDdN6aZhvb2hep8500bkB7edBLWfc4oX9Ix8L5icbhKqxEQ6zCafK-0Pm3ifo4cShChGjJlCG_z4hK9_zHCaX-bVRChttI2_Mr5YeQY9zYRAaML_jloyFBADdofq0-FUX-ungZLSehCudM4AQKm6MSmQ4cboN-iV0000__y30000)

## Các ca sử dụng chính:
* Thống kê các giao dịch ngân hàng
## Đặc tả ca sử dụng
### Ca sử dụng: Thống kê các giao dịch ngân hàng
* Tên: Thống kê giao dịch ngân hàng
* Tác nhân: Người dùng, Hệ thống phân tích
* Mô tả: Người dùng tải lên tệp sao kê, hệ thống phân tích và thống kê kết quả giao dịch.
* Tiền điều kiện: Tệp sao kê hợp lệ.
* Luồng sự kiện chính: Người dùng tải tệp sao kê lên hệ thống -> Hệ thống phân tích các giao dịch -> Hệ thống tạo báo cáo thống kê -> Người dùng xem kết quả -> Kết quả được lưu trữ
* Luồng sự kiện phụ:
* + Lỗi tệp sao kê: Tệp không hợp lệ.
* + Không có giao dịch: Không có dữ liệu để phân tích.
* + Lỗi phân tích: Hệ thống không thể phân tích tệp.
* Hậu điều kiện:
* + Kết quả phân tích được lưu trữ và báo cáo có sẵn.
* Ngoại lệ:
* + Tệp sao kê không hợp lệ: Lỗi định dạng tệp.
* + Lỗi cơ sở dữ liệu: Không thể lưu kết quả.
##Yêu cầu phi chức năng
* Yêu cầu hiệu suất:

Hệ thống phải xử lý tối thiểu 5000 giao dịch trong 5 giây để đảm bảo hiệu suất khi xử lý tệp lớn.


