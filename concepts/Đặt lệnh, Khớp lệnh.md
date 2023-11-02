> **_Lệnh chứng khoán_** - những thao tác nhà đầu tư thực hiện để mua bán chứng khoán trên sàn nhằm thu lợi nhuận.

* Mỗi loại lệnh sẽ có những đặc điểm khác nhau, cần lựa chọn lệnh phù hợp để hạn chế rủi ro.

### 1. Lệnh giao dịch tại mức giá khớp lệnh xác định giá mở cửa (ATO)
* Lệnh mua hoặc bán chứng khoán ở giá mở cửa, chỉ có hiệu lực ở phiên ATO
* Được ưu tiên hơn lệnh giới hạn (LO)
* Nếu lệnh ATO ko được thực hiện hoàn tất sau tgian xác định giá mở cửa -> Bị hủy
* Không cần nhập giá, mức giá khớp lệnh được hệ thống xác định.

### 2. Lệnh giới hạn (LO)
* Cho phép nhà đầu tư mua hoặc bán chứng khoán với mức giá xác định.
* Nếu giá cổ phiếu không thỏa mãn lệnh đã đặt, giao dịch sẽ không diễn ra.

_Ex: cổ phiếu A đang ở mức 20.000đ, bạn đặt lệnh mua với giá 19.000đ. Nếu có người bán cổ phiếu này với giá nhỏ hơn hoặc bằng 19.000đ, lệnh của bạn sẽ được khớp. Ngược lại, nếu giá vẫn ở mức 20.000đ hoặc cao hơn thì sẽ không có giao dịch nào cả._

* Cho phép thiết lập giao dịch với mức giá mua cao nhất hoặc mức giá bán thấp nhất có thể chấp nhận
  * Lệnh có hiệu lực sau khi nhập vào hệ thống, kéo dài tới cuối ngày giao dịch hoặc cho đến khi lệnh bị hủy bỏ.

### 3. Lệnh thị trường trên sàn HoSE (MP)
* Lệnh mua với giá thấp nhất đang được chào bán, hoặc bán ngay lập tức với giá chào mua cao nhất.

_Ex: bạn đặt lệnh MP để mua 3000 cổ phiếu A. Tại thời điểm đặt lệnh sẽ có những mức giá tương ứng với khối lượng được các bên rao bán như sau:_
* _80.000 đồng – khối lượng 500 cổ phiếu_
* _80.100 đồng – khối lượng 2000 cổ phiếu_
* _80.200 đồng – khối lượng 3000 cổ phiếu_

_Nếu bạn đặt mua 3000 cổ phiếu A, thì 500 cổ phiếu đầu tiên sẽ khớp lệnh với giá 80.000/1 cổ phiếu, 2000 cổ phiếu tiếp theo sẽ khớp lệnh với giá 80.1000/1 cổ phiếu; 500 cổ phiếu còn lại sẽ khớp lệnh với giá 80.200/1 cổ phiếu._

* Lệnh không đảm bảo về giá, nhưng lệnh luôn được thực hiện ngay lập tức -> Phù hợp với ý định mua bán cổ phiếu nhanh chóng.

### 4. Lệnh thị trường HNX
* Lệnh mua với giá chào bán thấp nhất hiện có trên thị trường hoặc bán với giá chào mua cao nhất trong khoảng thời gian khớp lệnh liên tiếp
* Có 3 loại lệnh:
   * **Lệnh MAK**: thực hiện toàn bộ hoặc 1 phần, phần còn lại của lệnh sẽ bị hủy ngay sau khi khớp lệnh
   * **Lệnh MOK**: lệnh bị hủy trên hệ thống ngay sau khi nhập nếu không thể khớp lệnh toàn bộ.
   * **Lệnh MTL**: lệnh có thể được thực hiện toàn bộ hoặc 1 phần, phần còn lại của các lệnh sẽ trở thành lệnh LO
 
### 5. Lệnh chờ (Lệnh điều kiện)
* Lệnh có điều kiện kèm theo khi đặt lệnh, sẽ ở trạng thái chờ và chỉ đẩy ra thị trường khi thỏa mãn các điều kiện trước.
* Cho phép nhà đầu tư dễ dàng mua/bán ở mức giá mục tiêu định trước.
* Phổ biến với thị trường phái sinh
* Có 4 loại lệnh điều kiện:
   * Lệnh `TCO` - lệnh điều kiện với thời gian
   * Lệnh `PRO` - lệnh tranh mua hoặc tranh bán
   * Lệnh `ST` - lệnh dừng
   * Lệnh `TS` - lệnh xu hướng  

### 6. Lệnh giao dịch tại mức giá khớp lệnh xác định giá đóng cửa (ATC)
* Đặt mua hoặc bán chứng khoán với mức giá đóng cửa, chỉ có hiệu lực tại phiên ATC (14h30 - 14h45)
* Giá được xác định thông qua các lệnh LO được đặt. (Nếu chỉ có lệnh ATC tại sổ lệnh thì phiên ATC không xác định được giá đóng cửa.)
* Lệnh ATC sẽ được ưu tiên khớp lệnh hơn so với lệnh LO.
* Hệ thống sẽ tự động hủy đối với những phần không được khớp của lệnh ATC trong phiên.

### 7. Lệnh giao dịch khớp lệnh sau giờ (PLO)
* Lệnh hạn mức dùng để mua hoặc bán chứng khoán trong phiên giao dịch ngoài giờ.
* Giá đặt lệnh PLO là giá đóng cửa của phiên giao dịch ngày hôm đó.
* Sẽ được đặt trong khung h 14h45 - 15h00
  * Lệnh đã vào hệ thống thì không thể hủy, sửa
  * Sẽ được khớp ngay lập tức khi có lệnh tương ứng.  

---
> _**Khớp lệnh** - quá trình mà một sàn chứng khoán ghép một hoặc nhiều lệnh mua tự nguyện với một hoặc nhiều lệnh bán để thực hiện giao dịch._

* Là quá trình xác định và thực hiện giao dịch giữa các yêu cầu bằng nhau và trái ngược nhau đối với một chứng khoán. (mua/bán cùng 1 mức giá)

### Các nguyên tắc khi thực hiện khớp lệnh
* Ưu tiên về giá:
  * Có mức giá tốt hơn (mua cao hơn hoặc bán thấp hơn) sẽ được ưu tiên trước

* Ưu tiên về thời gian
  * Nếu nhiều lệnh có cùng giá, lệnh được đặt trước (hoặc được gửi trước) sẽ được ưu tiên.

* Ưu tiên khách hàng
  * Lệnh của khách hàng cá nhân (cả người mua và người bán) sẽ được ưu tiên hơn lệnh của các nhà giao dịch chuyên nguyện hoặc các quỹ đầu tư lớn

* Ưu tiên khối lượng
  * Nếu nhiều lệnh cùng giá, thì lệnh với số lượng lớn hơn sẽ được ưu tiên.

### Quá trình khớp lệnh
* Là trách nhiệm của các chuyên gia thị trường và nhà cung cấp chứng khoán trên thị trường.

* Các lệnh mua và bán là tương thích nếu giá tối đa của lệnh mua vượt qua hoặc bằng giá tối thiểu của lệnh bán.

* Hệ thống khớp lệnh hoạt động nhanh chóng và chính xác để tối đa hóa khối lượng giao dịch cũng như giúp nhà đầu tư đạt được mức giá lý tưởng.

* FIFO và Pro - rata (Theo tỷ lệ) là hai thuật toán phổ biến nhất để khớp lệnh
  * FIFO: các lệnh mua có cùng mức giá tối đa được ưu tiên dựa vào thời điểm đặt giá (ưu tiên cho lệnh mua đầu tiên), đồng thời cũng ưu tiên hơn so với các lệnh mua ở mức giá thấp hơn
  * Pro - rata: ưu tiên cho lệnh mua có giá cao nhất, các lệnh mua có cùng mức giá cao nhất được khớp tương ứng với kích cỡ lệnh.

_Ex:
Ví dụ: khi lệnh mua 300 cổ phiếu và 100 cổ phiếu của cùng một chứng khoán đang hoạt động trong hệ thống đồng thời một lệnh bán tương thích gồm 300 cổ phiếu được kích hoạt lệnh bán sẽ không thể thực hiện cả hai lệnh mua. Thuật toán Pro - rata sẽ khớp 225 cổ phiếu với lệnh mua 300 cổ phiếu và 75 cổ phiếu với lệnh mua 100 cổ phiếu. Do đó cả hai lệnh mua đều được lấp đầy một phần._

### Các loại khớp lệnh
* 2 loại: **Khớp lệnh định kỳ** và **Khớp lệnh liên tục**