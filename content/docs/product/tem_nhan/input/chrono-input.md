---
bookFlatSection: true
weight: 30
type: docs
title: Tham Số Thời Gian
url: /tem_nhan/chrono-input
---

# Tham Số Thời Gian Cho In Tem nhãn

Dưới đây là những tham số liên quan tới thiết lập thời gian mà cần người dùng cần nhập để tạo đơn in Tem nhãn.

## Thông số thời gian máy
**Tốc độ planning và thời gian setup theo máy**

- **Thời gian setup máy flexo cuộn**
  * *Setup web, bản, mực, register và bế inline theo recipe máy.*
  * *Đơn vị*: Phút
  * *Mã*: TCIPRESSSETUP
  * *Kí hiệu*: {{< katex >}}T_{p,setup}{{< /katex >}}

- **Tốc độ planning máy flexo cuộn**
  * *Tốc độ web planning sau hiệu chỉnh theo vật liệu, màu, bế và OEE.*
  * *Đơn vị*: m/Phút
  * *Mã*: TCIPRESSSPEED
  * *Kí hiệu*: {{< katex >}}v_p{{< /katex >}}

- **Thời gian setup máy chia cuộn**
  * *Setup dao, lõi, hướng quấn và bộ đếm cuộn thành phẩm.*
  * *Đơn vị*: Phút
  * *Mã*: TCISLITSETUP
  * *Kí hiệu*: {{< katex >}}T_{s,setup}{{< /katex >}}

- **Tốc độ planning chia cuộn**
  * *Tốc độ web planning của máy chia/kiểm tra/rewind offline.*
  * *Đơn vị*: m/Phút
  * *Mã*: TCISLITSPEED
  * *Kí hiệu*: {{< katex >}}v_s{{< /katex >}}

- **Tốc độ planning cán màng tem**
  * *Tốc độ web planning của cụm cán màng cuộn.*
  * *Đơn vị*: m/Phút
  * *Mã*: TCILAMSPEED
  * *Kí hiệu*: {{< katex >}}v_l{{< /katex >}}

- **Thời gian setup cán màng tem**
  * *Lắp cuộn màng, canh sức căng, nhiệt và áp lực lô ép.*
  * *Đơn vị*: Phút
  * *Mã*: TCILAMSETUP
  * *Kí hiệu*: {{< katex >}}T_{l,setup}{{< /katex >}}

- **Tốc độ planning ép nhũ**
  * *Tốc độ web planning của cụm ép nhũ, đã trừ hao dừng thay cuộn nhũ.*
  * *Đơn vị*: m/Phút
  * *Mã*: TCIFOILSPEED
  * *Kí hiệu*: {{< katex >}}v_f{{< /katex >}}

- **Thời gian setup ép nhũ**
  * *Lắp khuôn nhũ, cuộn nhũ, canh nhiệt, áp lực và register.*
  * *Đơn vị*: Phút
  * *Mã*: TCIFOILSETUP
  * *Kí hiệu*: {{< katex >}}T_{f,setup}{{< /katex >}}

- **Thời gian hoàn thiện khác**
  * *Ô nhập tay cho các khâu hoàn thiện chưa được mô hình hoá (phủ varnish offline, embossing, in lụa, đánh số, đục lỗ, đóng gói cuộn).*
  * *Đơn vị*: Phút
  * *Mã*: TCIOTHER
  * *Kí hiệu*: {{< katex >}}T_{other}{{< /katex >}}



