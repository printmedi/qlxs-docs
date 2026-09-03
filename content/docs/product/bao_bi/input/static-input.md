---
bookFlatSection: true
weight: 10
type: docs
title: Đơn Giá Và Hằng Số
url: /bao_bi/static-input
---

# Đơn Giá Và Hằng Số In Bao bì hộp

Những tham số dưới đây là các đơn giá hoặc hằng số. Khác với tham số bình thường, chúng có thể được thiết lập để sử dụng cho nhiều đơn khác nhau, giữa nhiều phương thức gia công khác nhau khi in Bao bì hộp.

## Đơn giá nguyên vật liệu
**Giá giấy, mực và bản offset**

- **Đơn giá giấy hộp**
  * *Đơn giá đúng mã giấy/carton theo tấn.*
  * *Đơn vị*: VNĐ/Tấn
  * *Mã*: BBSTAPAPERPRICE
  * *Kí hiệu*: {{< katex >}}P_s{{< /katex >}}
- **Đơn giá mực offset**
  * *Đơn giá mực theo hệ mực và màu thực tế.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: BBSTAINKPRICE
  * *Kí hiệu*: {{< katex >}}P_i{{< /katex >}}
- **Đơn giá một bản offset**
  * *Giá chế một bản kẽm theo khổ tờ in được chọn.*
  * *Đơn vị*: VNĐ/Bản
  * *Mã*: BBSTAPLATEPRICE
  * *Kí hiệu*: {{< katex >}}P_p{{< /katex >}}
- **Định mức màng mực offset tại 100% phủ**
  * *Khối lượng mực hiệu lực trên một m² cho một màu ở 100% phủ.*
  * *Đơn vị*: g/m²
  * *Mã*: BBSTAINKFILM
  * *Kí hiệu*: {{< katex >}}f_i{{< /katex >}}
## Đơn giá sản xuất
**Chi phí giờ máy in và chi phí đơn hàng**

- **Đơn giá giờ máy in offset**
  * *Chi phí cho mỗi giờ sử dụng máy in.*
  * *Đơn vị*: VNĐ/Giờ
  * *Mã*: BBSTAPRESSHOUR
  * *Kí hiệu*: {{< katex >}}P_m{{< /katex >}}
- **Chi phí đơn hàng khác**
  * *Chi phí cố định khác được nhà máy phê duyệt.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBSTAOTHER
  * *Kí hiệu*: {{< katex >}}C_o{{< /katex >}}
## Hằng số kỹ thuật
**Hao hụt, hình học kiểu hộp và khoảng cách nesting**

- **Tỷ lệ hao hụt thành phẩm hộp**
  * *Hao hụt sau in thuộc sản lượng giao; hiệu chuẩn từ QC thực tế.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: BBSTAFINLOSS
  * *Kí hiệu*: {{< katex >}}w_f{{< /katex >}}
- **Tỷ lệ hao hụt chạy in hộp**
  * *Hao hụt biến đổi theo tờ chạy, tách khỏi tờ setup.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: BBSTARUNLOSS
  * *Kí hiệu*: {{< katex >}}w_r{{< /katex >}}
- **Số tờ căn chỉnh máy in hộp**
  * *Số tờ dùng để căn chỉnh màu và độ chồng khít trước khi in chính thức.*
  * *Đơn vị*: Tờ
  * *Mã*: BBSTASETUPSHEETS
  * *Kí hiệu*: {{< katex >}}N_{setup}{{< /katex >}}
- **Độ rộng tai dán**
  * *Chiều rộng phần mép dùng để bôi keo và dán thân hộp.*
  * *Đơn vị*: mm
  * *Mã*: BBSTAGLUEFLAP
  * *Kí hiệu*: {{< katex >}}g{{< /katex >}}
- **Tỷ lệ chiều dài nắp chính**
  * *Chiều dài nắp chính = chiều rộng hộp × tỷ lệ này.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: BBSTAMAINFLAP
  * *Kí hiệu*: {{< katex >}}r_m{{< /katex >}}
- **Tỷ lệ chiều dài tai bụi**
  * *Chiều dài tai bụi = chiều rộng hộp × tỷ lệ này.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: BBSTADUSTFLAP
  * *Kí hiệu*: {{< katex >}}r_d{{< /katex >}}
- **Khe hở giữa các tai**
  * *Khe kỹ thuật tại đường phân chia các tai gấp.*
  * *Đơn vị*: mm
  * *Mã*: BBSTAFLAPGAP
  * *Kí hiệu*: {{< katex >}}e{{< /katex >}}
- **Hệ số bù đường cấn theo độ dày**
  * *Bù thêm kích thước theo độ dày giấy khi dựng các mặt hộp; đặt 0 nếu không cần bù.*
  * *Đơn vị*: Hệ số
  * *Mã*: BBSTACREASECOMP
  * *Kí hiệu*: {{< katex >}}k_t{{< /katex >}}
- **Khoảng cách giữa hai khuôn hộp**
  * *Khoảng trống tối thiểu phải giữ giữa hai khuôn hộp khi xếp trên cùng một tờ.*
  * *Đơn vị*: mm
  * *Mã*: BBSTANESTGAP
  * *Kí hiệu*: {{< katex >}}d{{< /katex >}}
- **Lề an toàn tờ in**
  * *Khoảng trống tối thiểu giữ quanh mép tờ in khi xếp khuôn hộp.*
  * *Đơn vị*: mm
  * *Mã*: BBSTASAFEMARGIN
  * *Kí hiệu*: {{< katex >}}m{{< /katex >}}


