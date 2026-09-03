---
bookFlatSection: true
weight: 20
type: docs
title: Tham Số Nguyên Vật Liệu
url: /tem_nhan/material-input
---

# Tham Số Nguyên Vật Liệu Cho In Tem nhãn

Dưới đây là những tham số liên quan tới thiết lập nguyên vật liệu mà cần người dùng cần nhập để tạo đơn in Tem nhãn.

## Thông tin đơn tem
**Sản lượng và kích thước tem khách hàng**

- **Số lượng tem cần giao**
  * *Số tem tốt khách hàng yêu cầu.*
  * *Đơn vị*: Tem
  * *Mã*: TMINQTY
  * *Kí hiệu*: {{< katex >}}Q{{< /katex >}}

- **Chiều rộng tem**
  * *Một cạnh thành phẩm; engine được phép hoán đổi hai cạnh khi sinh candidate.*
  * *Đơn vị*: mm
  * *Mã*: TMINWIDTH
  * *Kí hiệu*: {{< katex >}}w{{< /katex >}}

- **Chiều dài tem**
  * *Cạnh còn lại của tem thành phẩm.*
  * *Đơn vị*: mm
  * *Mã*: TMINLENGTH
  * *Kí hiệu*: {{< katex >}}h{{< /katex >}}

## Không sử dụng
**Section tương thích schema; Tem không có bìa**

## Không sử dụng
**Section tương thích schema; Tem không có ruột**

## Candidate khổ cuộn và repeat
**Một phương án cụ thể do engine sinh để generator kiểm tra và tính**

- **Khoảng cách tem ngang**
  * *Khoảng cách giữa hai tem kề nhau theo chiều ngang web.*
  * *Đơn vị*: mm
  * *Mã*: TMINGAPX
  * *Kí hiệu*: {{< katex >}}g_x{{< /katex >}}

- **Khoảng cách tem dọc**
  * *Khoảng cách từ mép tem này đến tem tiếp theo theo chiều chạy; gồm gap qua biên repeat.*
  * *Đơn vị*: mm
  * *Mã*: TMINGAPY
  * *Kí hiệu*: {{< katex >}}g_y{{< /katex >}}

- **Khổ cuộn chạy**
  * *Khổ web cụ thể của candidate do engine gửi, không phải danh sách khổ để generator tự thử.*
  * *Đơn vị*: mm
  * *Mã*: TMINWEB
  * *Kí hiệu*: {{< katex >}}W{{< /katex >}}

- **Chiều dài repeat**
  * *Repeat in/bế chung của candidate flexo inline.*
  * *Đơn vị*: mm
  * *Mã*: TMINREPEAT
  * *Kí hiệu*: {{< katex >}}R{{< /katex >}}

- **Số tem ngang**
  * *Số tem theo chiều ngang web của candidate do engine sinh.*
  * *Đơn vị*: Tem
  * *Mã*: TMINACROSS
  * *Kí hiệu*: {{< katex >}}n_x{{< /katex >}}

- **Số tem quanh repeat**
  * *Số tem theo chiều chạy trong một repeat của candidate do engine sinh.*
  * *Đơn vị*: Tem
  * *Mã*: TMINAROUND
  * *Kí hiệu*: {{< katex >}}n_y{{< /katex >}}

- **Khổ web tối đa của máy**
  * *Khổ vật liệu lớn nhất máy flexo cuộn tiếp nhận.*
  * *Đơn vị*: mm
  * *Mã*: TMINWEBMAX
  * *Kí hiệu*: {{< katex >}}W_{max}{{< /katex >}}

- **Khổ in hữu dụng tối đa**
  * *Bề rộng hình ảnh/bế hữu dụng tối đa theo cấu hình máy.*
  * *Đơn vị*: mm
  * *Mã*: TMINPRINTMAX
  * *Kí hiệu*: {{< katex >}}P_{max}{{< /katex >}}

- **Repeat in tối thiểu**
  * *Repeat in nhỏ nhất máy/cấu hình hỗ trợ.*
  * *Đơn vị*: mm
  * *Mã*: TMINPRMIN
  * *Kí hiệu*: {{< katex >}}R_{p,min}{{< /katex >}}

- **Repeat in tối đa**
  * *Repeat in lớn nhất máy/cấu hình hỗ trợ.*
  * *Đơn vị*: mm
  * *Mã*: TMINPRMAX
  * *Kí hiệu*: {{< katex >}}R_{p,max}{{< /katex >}}

- **Repeat bế tối thiểu**
  * *Repeat bế inline nhỏ nhất máy/cấu hình hỗ trợ.*
  * *Đơn vị*: mm
  * *Mã*: TMINDRMIN
  * *Kí hiệu*: {{< katex >}}R_{d,min}{{< /katex >}}

- **Repeat bế tối đa**
  * *Repeat bế inline lớn nhất máy/cấu hình hỗ trợ.*
  * *Đơn vị*: mm
  * *Mã*: TMINDRMAX
  * *Kí hiệu*: {{< katex >}}R_{d,max}{{< /katex >}}

## Thông tin in và thành phẩm
**Màu, độ phủ và quy cách chia cuộn**

- **Số màu in flexo**
  * *Số màu/bản flexo của artwork.*
  * *Đơn vị*: Màu
  * *Mã*: TMINCOLORS
  * *Kí hiệu*: {{< katex >}}c{{< /katex >}}

- **Độ phủ trung bình mỗi màu**
  * *Độ phủ trung bình của một màu trên vùng web chạy.*
  * *Đơn vị*: %
  * *Mã*: TMINCOVERAGE
  * *Kí hiệu*: {{< katex >}}a{{< /katex >}}

- **Số tem tối đa mỗi cuộn thành phẩm**
  * *Giới hạn chia cuộn theo yêu cầu giao hàng; 0 nghĩa không giới hạn chia nhỏ, mỗi lane chạy thành một cuộn.*
  * *Đơn vị*: Tem/Cuộn
  * *Mã*: TMINROLLQTY
  * *Kí hiệu*: {{< katex >}}q_{roll}{{< /katex >}}



