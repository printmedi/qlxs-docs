---
bookFlatSection: true
weight: 10
type: docs
title: Đơn Giá Và Hằng Số
url: /tem_nhan/static-input
---

# Đơn Giá Và Hằng Số In Tem nhãn

Những tham số dưới đây là các đơn giá hoặc hằng số. Khác với tham số bình thường, chúng có thể được thiết lập để sử dụng cho nhiều đơn khác nhau, giữa nhiều phương thức gia công khác nhau khi in Tem nhãn.

## Đơn giá nguyên vật liệu
**Giá vật liệu tem, mực và bản flexo**

- **Đơn giá vật liệu tem tự dính**
  * *Giá mua toàn bộ construction gồm facestock, keo và liner.*
  * *Đơn vị*: VNĐ/m²
  * *Mã*: TSTALABELPRICE
  * *Kí hiệu*: {{< katex >}}P_{stock}{{< /katex >}}
- **Đơn giá mực flexo**
  * *Giá mực theo hệ mực và màu thực tế.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: TSTAINKPRICE
  * *Kí hiệu*: {{< katex >}}P_{ink}{{< /katex >}}
- **Đơn giá bản flexo theo diện tích**
  * *Chi phí bản flexo theo diện tích hình học của một repeat nhân số màu.*
  * *Đơn vị*: VNĐ/m²
  * *Mã*: TSTAPLATEPRICE
  * *Kí hiệu*: {{< katex >}}P_{plate}{{< /katex >}}
- **Định mức màng mực flexo tại 100% phủ**
  * *Khối lượng mực hiệu lực trên một m² tại 100% phủ cho một màu.*
  * *Đơn vị*: g/m²
  * *Mã*: TSTAINKFILM
  * *Kí hiệu*: {{< katex >}}f_{ink}{{< /katex >}}
## Đơn giá sản xuất
**Chi phí setup, chạy máy và chia cuộn**

- **Chi phí setup máy flexo**
  * *Chi phí cố định setup một job trên máy in cuộn.*
  * *Đơn vị*: VNĐ
  * *Mã*: TSTASETUPCOST
  * *Kí hiệu*: {{< katex >}}C_{setup}{{< /katex >}}
- **Chi phí chạy máy flexo theo mét**
  * *Chi phí biến đổi theo mét web thực tế đi qua máy.*
  * *Đơn vị*: VNĐ/m
  * *Mã*: TSTARUNCOST
  * *Kí hiệu*: {{< katex >}}C_{run,m}{{< /katex >}}
- **Chi phí chia cuộn theo mét**
  * *Chi phí biến đổi của công đoạn chia/rewind offline theo mét web.*
  * *Đơn vị*: VNĐ/m
  * *Mã*: TSTASLITCOST
  * *Kí hiệu*: {{< katex >}}C_{slit,m}{{< /katex >}}
- **Chi phí đơn hàng khác**
  * *Chi phí cố định khác đã được nhà máy phê duyệt.*
  * *Đơn vị*: VNĐ
  * *Mã*: TSTAOTHERCOST
  * *Kí hiệu*: {{< katex >}}C_{other}{{< /katex >}}
## Hằng số kỹ thuật
**Hao hụt, lề cuộn và định mức kỹ thuật**

- **Tỷ lệ hao hụt thành phẩm tem**
  * *Hao hụt sau in/bế/chia cuộn, dùng nâng sản lượng mục tiêu trước khi tính repeat.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: TSTAFINLOSS
  * *Kí hiệu*: {{< katex >}}w_f{{< /katex >}}
- **Tỷ lệ hao hụt chạy web**
  * *Hao hụt biến đổi theo chiều dài chạy, tách khỏi mét setup cố định.*
  * *Đơn vị*: Tỷ lệ
  * *Mã*: TSTARUNLOSS
  * *Kí hiệu*: {{< katex >}}w_r{{< /katex >}}
- **Mét vật liệu setup cố định**
  * *Web dùng cho lên màu, chồng màu, bế và ổn định sức căng trước phần chạy tốt.*
  * *Đơn vị*: m
  * *Mã*: TSTASETUPM
  * *Kí hiệu*: {{< katex >}}L_{setup}{{< /katex >}}
- **Lề biên cuộn mỗi bên**
  * *Phần biên không bố trí tem ở mỗi phía của web.*
  * *Đơn vị*: mm
  * *Mã*: TSTAEDGEMARGIN
  * *Kí hiệu*: {{< katex >}}e{{< /katex >}}


