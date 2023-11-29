## Phương thức lấy dữ liệu
Có hai cách chủ yếu được sử dụng để lấy dữ liệu từ các trang thông tin, các sàn giao dịch chứng khoán
* Fetch data from API:
    * Hợp pháp
    * Dữ liệu được đảm bảo tính toàn vẹn, cập nhật nhanh chóng
    * Có thể phát sinh chi phí
* Crawl data from website:
    * Một vài trường hợp sẽ là bất hợp pháp
    * Dữ liệu không được đảm bảo về tính toàn vẹn
    * Ít tốn chi phí

## Một các trường thông tin cần thu thập 

---
**Một vài chỉ số quan trọng**:
* `VN-Index` - chỉ số thể hiện xu hướng biến động giá của tất cả các cổ phiếu niêm yết và giao dịch tại HoSE
* `VN30-Index` - chỉ số giá của 30 cổ phiếu bluechip trên thị trường
* `HNX-Index` - chỉ số được tính toán dựa trên biến động giá cả tất cổ phiếu niêm yết và giao dịch tại HNX
* `UPCOM-Index` - chỉ số được tính toán dựa trên biến động giá tất cả các cổ phiếu giao dịch trên thị trường UPCoM
---

* Mã chứng khoán (Code)

### Các thông số thuộc bảng giá chứng khoán

* Giá tham chiếu/TC (Close price): 
    * là mức giá đóng cửa tại phiên giao dịch gần nhất trước đó 
    * được lấy làm cơ sở để tính toán biên độ giao dịch của cổ phiếu trong phiên

(_Riêng sàn UPCoM, giá TC được tính bằng giá bình quân của phiên giao dịch gần nhất._)

* Giá Trần (Highest price): 
    * là mức giá cao nhất mà có thể đặt lệnh mua hoặc bán chứng khoán trong ngày giao dịch.
    * HoSE: Trần = TC + 7%, HNX = TC + 10%, UPCoM = TC + 15%

* Giá Sàn (Lowest price):
    * là mức giá thấp nhất mà bạn có thể đặt lệnh mua hoặc bán chứng khoán trong ngày giao dịch.
    * Biên độ tương ứng với giá trần

* Bên mua: 3 mức giá đặt mua tốt nhất và khối lượng đặt mua tương ứng

* Bên bán: 3 mức giá bán tốt nhất và khối lượng bán tương ứng

* Khớp lệnh: hiển thị mức giá khớp lệnh gần nhất của một cổ phiếu
    * Giá khớp lệnh
    * Khối lượng khớp lệnh
    * Biên độ giá so với tham chiếu (biên độ, phần trăm)

* Tổng khối lượng (): khối lượng cổ phiếu đó được giao dịch trong một phiên

* Giá cao: giá khớp ở mức cao nhất trong phiên (có thể không phải là giá trần)

* Giá thấp: giá khớp ở mức thấp nhất trong phiên (có thể không phải là giá trần)

* Đầu tư nước ngoài (ĐTNN): khối lượng cổ phiếu được giao dịch của nhà đầu tư nước ngoài
    * NN mua, NN bán, NN dư

### Các thông số thuộc lịch sử giá

* Ngày (Date): ngày giao dịch

* Thay đổi: mức tăng/giảm của giá trị cổ phiếu (giá trị, phần trăm)

* Giá đóng cửa

* Giá đóng cửa điều chỉnh (Modifiable price): là giá đóng cửa được điều chỉnh lại để xác định giá trị chính xác trong cổ phiếu.
    * Trong TH công ty có các hoạt động làm thay đổi số lượng cổ phiếu.

Ex: Công ty trả cổ tức bằng cổ phiếu, chia tách cổ phiếu -> Làm tăng lượng cổ phiếu, ko thay đổi giá trị vốn hóa -> giá trị cổ phiếu giảm

* Thông tin giao dịch khớp lệnh:
    * Khối lượng cổ phiếu được khớp
    * Tổng giá trị khớp lệnh

* Thông tin giao dịch thỏa thuận:
    * Khối lượng cổ phiếu được thỏa thuận
    * Tổng giá trị thỏa thuận

> _**Giao dịch thỏa thuận**_ - phương tức bên mua và bên bán tự thỏa thuận về giá, khối lượng gd, hình thức chứng khoán rồi thông báo cho công ty chứng khoán.

* Giá mở cửa

* Giá cao nhất: giá cao nhất được giao dịch

* Giá thấp nhất: giá thấp nhất được giao dịch

* Giá trung bình

## Tổ chức CSDL

* Dự định tổ chức cơ sở dữ liệu để lưu trữ thông tin về: bảng giá chứng khoán và lịch sử giá của chứng khoán

* Một table chứa thông tin bảng giá chứng khoán (PK: Mã chứng khoán)
    * Table cần update thông tin về bẳng giá liên tục (tần suất: 5p/1 lần ?)
* Một table chứa thông tin lịch sử giá của chứng khoán (PK: id, FK: Mã chứng khoán)
    * Cập nhật lịch sử giá cuối mỗi ngày

**Yêu cầu**: csdl cần có tốc độ truy vấn theo chiều dọc nhanh, có khả năng mở rộng theo chiều dọc
