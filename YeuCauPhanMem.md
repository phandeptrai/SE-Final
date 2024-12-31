## Chức năng chính của hệ thống:

Nhập dữ liệu giao dịch: Tải lên tệp sao kê ngân hàng (CSV, Excel, PDF).
Phân tích giao dịch: Tính toán thống kê giao dịch, phân loại theo các tiêu chí.
Lưu trữ kết quả phân tích: Lưu kết quả vào cơ sở dữ liệu.
## Tác nhân liên quan:

Người dùng: Tải lên tệp sao kê, xem kết quả phân tích, yêu cầu báo cáo.
Hệ thống phân tích: Xử lý và phân tích dữ liệu giao dịch.
Biểu đồ ca sử dụng
## Biểu dồ hệ thống
![Diagram](https://www.planttext.com/plantuml/png/HCmn2i8m5CRnFQTuk7i5gMw2M44ly4X36fgcchoW8iuEtaBdedCxT2XuZvp0AqZZqEqRVj__stQ98xJaIyrGw-fOgfCoaZ7aL5dmJbXc1ISqKWjOe2csX2HAOSZD3UgpKqR2XJ7l14SdOBBEGrFl8Glj2xGAxSrF01qiHx79-uS1wckUWrHO3VREyyXs8rjztXx83fqYD1t1mOVc6LNAheEpC9tzmt75RrmfIuJ9VAb_0000__y30000)

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


