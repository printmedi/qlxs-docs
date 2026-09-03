---
bookFlatSection: true
weight: 40
type: docs
title: Tính Toán Nguyên Vật Liệu
url: /tem_nhan/material-calculate
---

# Kết Quả Tính Toán Nguyên Vật Liệu Cho In Tem nhãn

Dưới đây là những kết quả tính toán liên quan tới giá trị nguyên vật liệu cho đơn in Tem nhãn.

## Không sử dụng
**Section tương thích schema; Tem không có bìa**

## Không sử dụng
**Section tương thích schema; Tem không có ruột**

## Chi phí
**Chi phí vật liệu, mực, bản và sản xuất**

- **Chi phí vật liệu tem**
  * *Tổng diện tích web nhân đơn giá construction.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTSTOCK
  * *Kí hiệu*: {{< katex >}}C_s{{< /katex >}}

- **Chi phí bản flexo**
  * *Diện tích bản hình học nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTPLATE
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}

- **Chi phí mực flexo**
  * *Khối lượng mực nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTINK
  * *Kí hiệu*: {{< katex >}}C_i{{< /katex >}}

- **Chi phí chạy máy flexo**
  * *Setup cố định cộng chi phí theo mét web thực chạy; bế inline không cộng lại mét chạy.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTPRESS
  * *Kí hiệu*: {{< katex >}}C_{press}{{< /katex >}}

- **Chi phí chia cuộn**
  * *Chi phí chia/rewind offline theo mét web.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTSLIT
  * *Kí hiệu*: {{< katex >}}C_{slit}{{< /katex >}}

- **Chi phí đơn hàng**
  * *Tổng vật liệu, bản, mực, chạy máy, chia cuộn và chi phí khác.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTORDER
  * *Kí hiệu*: {{< katex >}}C_o{{< /katex >}}

- **Đơn giá tính toán mỗi tem**
  * *Chi phí đơn hàng chia số tem tốt cần giao; chưa phải giá bán.*
  * *Đơn vị*: VNĐ/Tem
  * *Mã*: TMCCOSTUNIT
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}

## Sản lượng và hình học cuộn
**Repeat, mét chạy, diện tích, hao hụt và validation**

- **Số tem mục tiêu trước hoàn thiện**
  * *Sản lượng giao đã nâng theo hao hụt thành phẩm riêng.*
  * *Đơn vị*: Tem
  * *Mã*: TMCGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}

- **Số tem mỗi repeat**
  * *Tích số tem ngang và số tem quanh repeat.*
  * *Đơn vị*: Tem/Repeat
  * *Mã*: TMCPERREPEAT
  * *Kí hiệu*: {{< katex >}}N_R{{< /katex >}}

- **Số repeat cần chạy**
  * *Số repeat nguyên cần chạy để đạt sản lượng mục tiêu trước hao hụt.*
  * *Đơn vị*: Repeat
  * *Mã*: TMCREPEATS
  * *Kí hiệu*: {{< katex >}}N_{repeat}{{< /katex >}}

- **Tổng tem bố trí được**
  * *Số repeat nhân số tem trên repeat trước loại thành phẩm.*
  * *Đơn vị*: Tem
  * *Mã*: TMCPRODUCED
  * *Kí hiệu*: {{< katex >}}Q_p{{< /katex >}}

- **Số tem sản xuất vượt lượng giao**
  * *Chênh lệch hình học giữa tổng tem bố trí và số lượng khách hàng yêu cầu; gồm phần dự phòng hao hụt.*
  * *Đơn vị*: Tem
  * *Mã*: TMCOVERRUN
  * *Kí hiệu*: {{< katex >}}Q_o{{< /katex >}}

- **Chiều dài web thuần**
  * *Số repeat nhân repeat, chưa gồm hao hụt chạy và mét setup.*
  * *Đơn vị*: m
  * *Mã*: TMCNETLEN
  * *Kí hiệu*: {{< katex >}}L_n{{< /katex >}}

- **Tổng chiều dài web cần chạy**
  * *Chiều dài thuần đã bù hao hụt chạy, sau đó cộng mét setup cố định.*
  * *Đơn vị*: m
  * *Mã*: TMCTOTALLEN
  * *Kí hiệu*: {{< katex >}}L_t{{< /katex >}}

- **Tổng diện tích vật liệu tem**
  * *Toàn bộ web mua/chạy gồm setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: TMCAREA
  * *Kí hiệu*: {{< katex >}}A_t{{< /katex >}}

- **Diện tích tem thành phẩm giao**
  * *Diện tích hình chữ nhật của lượng tem giao, không gồm gap và liner xung quanh.*
  * *Đơn vị*: m²
  * *Mã*: TMCDELIVEREDAREA
  * *Kí hiệu*: {{< katex >}}A_l{{< /katex >}}

- **Diện tích vật liệu ngoài tem giao**
  * *Tổng diện tích web trừ diện tích hình học tem giao; gồm liner giữa tem, biên, setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: TMCWASTEAREA
  * *Kí hiệu*: {{< katex >}}A_w{{< /katex >}}

- **Tỷ lệ diện tích ngoài tem giao**
  * *Phần diện tích web không trở thành diện tích hình học tem giao.*
  * *Đơn vị*: %
  * *Mã*: TMCWASTEPCT
  * *Kí hiệu*: {{< katex >}}U_w{{< /katex >}}

- **Tổng diện tích bản flexo**
  * *Diện tích khổ cuộn nhân repeat và số màu; bootstrap hình học, production dùng kích thước bản thực tế.*
  * *Đơn vị*: m²
  * *Mã*: TMCPLATEAREA
  * *Kí hiệu*: {{< katex >}}A_p{{< /katex >}}

- **Khối lượng mực flexo**
  * *Diện tích web nhân số màu, độ phủ trung bình và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: TMCINKKG
  * *Kí hiệu*: {{< katex >}}M_i{{< /katex >}}

- **Số cuộn thành phẩm**
  * *Số cuộn giao khách; khi không giới hạn chia nhỏ, mỗi lane ngang tạo một cuộn.*
  * *Đơn vị*: Cuộn
  * *Mã*: TMCROLLS
  * *Kí hiệu*: {{< katex >}}N_{roll}{{< /katex >}}

- **Số tem ngang/quanh hợp lệ**
  * *1 nếu hai số lượng là số nguyên dương.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDCOUNT
  * *Kí hiệu*: {{< katex >}}V_n{{< /katex >}}

- **Bố trí tem vừa khổ cuộn và repeat**
  * *1 nếu candidate vừa theo hướng gốc hoặc hướng hoán đổi dài-rộng; generator không nhận input hướng xoay riêng.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDLAYOUT
  * *Kí hiệu*: {{< katex >}}V_l{{< /katex >}}

- **Khổ cuộn trong giới hạn máy**
  * *1 nếu khổ cuộn candidate không vượt khổ web tối đa của máy.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDWEB
  * *Kí hiệu*: {{< katex >}}V_W{{< /katex >}}

- **Repeat trong giới hạn in và bế**
  * *1 nếu repeat candidate nằm đồng thời trong khoảng của cụm in và cụm bế inline.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDREPEAT
  * *Kí hiệu*: {{< katex >}}V_R{{< /katex >}}



