---
bookFlatSection: true
weight: 40
type: docs
title: Tính Toán Nguyên Vật Liệu
url: /bao_bi/material-calculate
---

# Kết Quả Tính Toán Nguyên Vật Liệu Cho In Bao bì hộp

Dưới đây là những kết quả tính toán liên quan tới giá trị nguyên vật liệu cho đơn in Bao bì hộp.

## Giấy và tờ chạy
**Sản lượng tờ, diện tích, khối lượng và hao hụt**

- **Số hộp mục tiêu trước hao hụt thành phẩm**
  * *Sản lượng giao nâng riêng theo hao hụt sau in.*
  * *Đơn vị*: Hộp
  * *Mã*: BBCGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}

- **Số tờ tốt cần có**
  * *Số hộp mục tiêu chia cho số hộp trên tờ.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCGOODSHEETS
  * *Kí hiệu*: {{< katex >}}N_g{{< /katex >}}

- **Số tờ cần chạy trước setup**
  * *Tờ tốt đã bù hao hụt biến đổi khi chạy in.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCRUNSHEETS
  * *Kí hiệu*: {{< katex >}}N_r{{< /katex >}}

- **Tổng số tờ chạy**
  * *Tờ chạy biến đổi cộng tờ setup cố định.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCTOTALSHEETS
  * *Kí hiệu*: {{< katex >}}N_t{{< /katex >}}

- **Số hộp bố trí vượt lượng giao**
  * *Sức chứa hình học của số tờ tốt trừ lượng giao.*
  * *Đơn vị*: Hộp
  * *Mã*: BBCOVERRUN
  * *Kí hiệu*: {{< katex >}}Q_o{{< /katex >}}

- **Tổng diện tích giấy chạy**
  * *Toàn bộ tờ chạy gồm setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: BBCSHEETAREA
  * *Kí hiệu*: {{< katex >}}A_s{{< /katex >}}

- **Khối lượng giấy hộp**
  * *Diện tích giấy chạy nhân định lượng.*
  * *Đơn vị*: kg
  * *Mã*: BBCPAPERKG
  * *Kí hiệu*: {{< katex >}}M_s{{< /katex >}}

- **Khối lượng mực offset**
  * *Diện tích tờ chạy nhân màu, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: BBCINKKG
  * *Kí hiệu*: {{< katex >}}M_i{{< /katex >}}

## Không sử dụng
**Section tương thích schema**

## Chi phí
**Chi phí giấy, mực, bản và máy in**

- **Chi phí giấy hộp**
  * *Khối lượng giấy nhân đơn giá theo tấn.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPAPER
  * *Kí hiệu*: {{< katex >}}C_s{{< /katex >}}

- **Chi phí mực hộp**
  * *Khối lượng mực nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTINK
  * *Kí hiệu*: {{< katex >}}C_i{{< /katex >}}

- **Chi phí bản offset**
  * *Số bản nhân đơn giá mỗi bản.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPLATE
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}

- **Chi phí máy in**
  * *Tổng thời gian in và setup nhân đơn giá giờ máy.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPRESS
  * *Kí hiệu*: {{< katex >}}C_m{{< /katex >}}

- **Chi phí đơn hàng**
  * *Tổng chi phí thuộc phạm vi model in hộp offset.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTORDER
  * *Kí hiệu*: {{< katex >}}C_o{{< /katex >}}

- **Đơn giá tính toán mỗi hộp**
  * *Chi phí đơn hàng chia sản lượng cần giao; chưa phải giá bán.*
  * *Đơn vị*: VNĐ/Hộp
  * *Mã*: BBCCOSTUNIT
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}

## Kiểm tra candidate
**Hiệu suất nesting và giới hạn tờ/máy**

- **Hiệu suất diện tích nesting**
  * *Tổng diện tích polygon hộp trên một tờ chia diện tích tờ vật lý.*
  * *Đơn vị*: %
  * *Mã*: BBCUTIL
  * *Kí hiệu*: {{< katex >}}U{{< /katex >}}

- **Số bản in hộp**
  * *Một bản cho mỗi màu và mỗi mặt in.*
  * *Đơn vị*: Bản
  * *Mã*: BBCPLATES
  * *Kí hiệu*: {{< katex >}}N_p{{< /katex >}}

- **Tổng lượt chạy máy in**
  * *Số pass màu nhân số pass mặt theo khả năng máy.*
  * *Đơn vị*: Lượt
  * *Mã*: BBCRUNS
  * *Kí hiệu*: {{< katex >}}R{{< /katex >}}

- **Số hộp trên tờ hợp lệ**
  * *1 khi số hộp/tờ là số nguyên dương.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDCOUNT
  * *Kí hiệu*: {{< katex >}}V_n{{< /katex >}}

- **Diện tích nesting hợp lệ**
  * *Kiểm tra bảo thủ rằng tổng diện tích polygon không vượt diện tích tờ; engine chịu trách nhiệm kiểm tra va chạm thật.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDAREA
  * *Kí hiệu*: {{< katex >}}V_l{{< /katex >}}

- **Tờ hộp vừa máy in**
  * *Cho phép xoay cả tờ 90 độ khi so với khổ máy.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDMACHINE
  * *Kí hiệu*: {{< katex >}}V_m{{< /katex >}}

- **Tờ hộp vừa máy bế**
  * *Cho phép xoay cả tờ 90 độ khi so với khổ máy bế đã chọn.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDDIECUT
  * *Kí hiệu*: {{< katex >}}V_d{{< /katex >}}



