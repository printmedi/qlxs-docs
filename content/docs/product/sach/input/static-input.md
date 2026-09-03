---
bookFlatSection: true
weight: 10
type: docs
title: Đơn Giá Và Hằng Số
url: /sach/static-input
---

# Đơn Giá Và Hằng Số In Sách

Những tham số dưới đây là các đơn giá hoặc hằng số. Khác với tham số bình thường, chúng có thể được thiết lập để sử dụng cho nhiều đơn khác nhau, giữa nhiều phương thức gia công khác nhau khi in Sách.

## Đơn giá nguyên vật liệu
**Giá thành nguyên vật liệu khác nhau**

- **Đơn giá giấy bìa**
  * *Giá mua một tấn giấy bìa tại nhà máy.*
  * *Đơn vị*: VNĐ/Tấn
  * *Mã*: MAPPCOV
  * *Kí hiệu*: {{< katex >}}P_{paper,cover}{{< /katex >}}
- **Đơn giá giấy ruột**
  * *Giá mua một tấn giấy ruột tại nhà máy.*
  * *Đơn vị*: VNĐ/Tấn
  * *Mã*: MAPPIN
  * *Kí hiệu*: {{< katex >}}P_{paper,text}{{< /katex >}}
- **Đơn giá bản offset**
  * *Chi phí vật tư bản theo diện tích bản ghi.*
  * *Đơn vị*: VNĐ/cm²
  * *Mã*: MAPPLATE
  * *Kí hiệu*: {{< katex >}}P_{plate}{{< /katex >}}
- **Đơn giá mực**
  * *Giá mực offset theo khối lượng.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: MAPINK
  * *Kí hiệu*: {{< katex >}}P_{ink}{{< /katex >}}
- **Đơn giá màng bìa**
  * *Giá màng cán theo diện tích.*
  * *Đơn vị*: VNĐ/m²
  * *Mã*: MAPFLM
  * *Kí hiệu*: {{< katex >}}P_{film}{{< /katex >}}
- **Định mức màng mực tại 100% phủ**
  * *Khối lượng màng mực quy ước trên một m² tại 100% độ phủ.*
  * *Đơn vị*: g/m²
  * *Mã*: SHRINKFILM
  * *Kí hiệu*: {{< katex >}}f_{ink}{{< /katex >}}
## Đơn giá công sản xuất
**Giá thành cho từng hoạt động sản xuất**

- **Chi phí chế bản mỗi bản**
  * *Chi phí dịch vụ chế bản trên mỗi bản offset.*
  * *Đơn vị*: VNĐ/Bản
  * *Mã*: SHRPREPRESS
  * *Kí hiệu*: {{< katex >}}C_{prepress}{{< /katex >}}
- **Chi phí setup mỗi khuôn-lượt**
  * *Chi phí cố định cho một khuôn trên một lượt chạy máy.*
  * *Đơn vị*: VNĐ
  * *Mã*: SHRPRINTSET
  * *Kí hiệu*: {{< katex >}}C_{setup}{{< /katex >}}
- **Chi phí mỗi lượt tờ qua máy**
  * *Chi phí biến đổi cho một tờ qua máy in trong một lượt.*
  * *Đơn vị*: VNĐ/Lượt tờ
  * *Mã*: SHRIMPR
  * *Kí hiệu*: {{< katex >}}C_{impression}{{< /katex >}}
- **Chi phí hoàn thiện mỗi tay sách**
  * *Chi phí theo tay sách cho các công đoạn được processing bật; với không khâu không được gồm chi phí khâu.*
  * *Đơn vị*: VNĐ/Tay
  * *Mã*: SHRSIGFIN
  * *Kí hiệu*: {{< katex >}}C_{signature}{{< /katex >}}
- **Chi phí hoàn thiện mỗi cuốn**
  * *Chi phí công/máy hoàn thiện theo cuốn; processing không khâu cộng vật tư keo riêng nên cấu hình này không được gồm tiền keo.*
  * *Đơn vị*: VNĐ/Cuốn
  * *Mã*: SHRBOOKFIN
  * *Kí hiệu*: {{< katex >}}C_{book}{{< /katex >}}
- **Chi phí đơn hàng khác**
  * *Chi phí cố định khác đã được nhà máy phê duyệt.*
  * *Đơn vị*: VNĐ
  * *Mã*: SHROTHER
  * *Kí hiệu*: {{< katex >}}C_{other}{{< /katex >}}
## Hằng số khác
**Những hằng số mặc định khác**

- **Tỷ lệ hao hụt thành phẩm**
  * *Tỷ lệ hao hụt sau in, nhập dạng thập phân.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: SHRFINLOSS
  * *Kí hiệu*: {{< katex >}}w_f{{< /katex >}}
- **Tỷ lệ hao hụt chạy bìa**
  * *Hao hụt biến đổi khi chạy bìa, chưa gồm tờ căn chỉnh.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: SHRCOVLOSS
  * *Kí hiệu*: {{< katex >}}w_{p,c}{{< /katex >}}
- **Tỷ lệ hao hụt chạy ruột**
  * *Hao hụt biến đổi khi chạy ruột, chưa gồm tờ căn chỉnh.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: SHRINLOSS
  * *Kí hiệu*: {{< katex >}}w_{p,t}{{< /katex >}}
- **Tờ căn chỉnh bìa mỗi khuôn-lượt**
  * *Số tờ make-ready của mỗi khuôn trên mỗi lượt chạy máy.*
  * *Đơn vị*: Tờ
  * *Mã*: SHRCOVMR
  * *Kí hiệu*: {{< katex >}}m_c{{< /katex >}}
- **Tờ căn chỉnh ruột mỗi khuôn-lượt**
  * *Số tờ make-ready của mỗi khuôn trên mỗi lượt chạy máy.*
  * *Đơn vị*: Tờ
  * *Mã*: SHRINMR
  * *Kí hiệu*: {{< katex >}}m_t{{< /katex >}}
- **Khoảng chừa nhíp**
  * *Phần mép tờ dành cho hệ thống nhíp máy in.*
  * *Đơn vị*: cm
  * *Mã*: SHRKCN
  * *Kí hiệu*: {{< katex >}}g{{< /katex >}}
- **Bleed mỗi cạnh**
  * *Phần tràn lề ở mỗi cạnh thành phẩm.*
  * *Đơn vị*: cm
  * *Mã*: SHRKCX
  * *Kí hiệu*: {{< katex >}}b{{< /katex >}}
- **Khoảng thang màu**
  * *Phần mép tờ dành cho thang kiểm soát màu.*
  * *Đơn vị*: cm
  * *Mã*: SHRKTM
  * *Kí hiệu*: {{< katex >}}c{{< /katex >}}
- **Hệ số hiệu chỉnh gáy sau khâu và ép**
  * *Hiệu chỉnh độ dày khối ruột sau khâu chỉ và nén gáy.*
  * *Đơn vị*: Hệ số
  * *Mã*: SHRSPINE
  * *Kí hiệu*: {{< katex >}}k_s{{< /katex >}}
- **Độ dày đóng cuốn tối thiểu**
  * *Giới hạn nhỏ nhất của dây chuyền vào bìa.*
  * *Đơn vị*: mm
  * *Mã*: SHRMINSPINE
  * *Kí hiệu*: {{< katex >}}s_{min}{{< /katex >}}
- **Độ dày đóng cuốn tối đa**
  * *Giới hạn lớn nhất của dây chuyền vào bìa.*
  * *Đơn vị*: mm
  * *Mã*: SHRMAXSPINE
  * *Kí hiệu*: {{< katex >}}s_{max}{{< /katex >}}


