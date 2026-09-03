---
bookFlatSection: true
weight: 40
type: docs
title: Tính Toán Nguyên Vật Liệu
url: /sach/material-calculate
---

# Kết Quả Tính Toán Nguyên Vật Liệu Cho In Sách

Dưới đây là những kết quả tính toán liên quan tới giá trị nguyên vật liệu cho đơn in Sách.

## Thông tin tính toán bìa
**Thông tin tín toán bìa**

- **Số khuôn bìa**
  * *Số khuôn bình bìa cần chạy.*
  * *Đơn vị*: Khuôn
  * *Mã*: MATCOVFORM
  * *Kí hiệu*: {{< katex >}}F_c{{< /katex >}}

- **Số lượt màu bìa**
  * *Số lần chạy để đủ màu theo số đơn vị in của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATCOVCP
  * *Kí hiệu*: {{< katex >}}r_{c,color}{{< /katex >}}

- **Số lượt mặt bìa**
  * *Số lần chạy để đủ mặt theo khả năng trở mặt của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATCOVSP
  * *Kí hiệu*: {{< katex >}}r_{c,side}{{< /katex >}}

- **Tổng lượt chạy bìa mỗi khuôn**
  * *Tích lượt màu và lượt mặt.*
  * *Đơn vị*: Lượt/Khuôn
  * *Mã*: MATCOVPASS
  * *Kí hiệu*: {{< katex >}}r_c{{< /katex >}}

- **Tờ bìa tốt tối thiểu**
  * *Tờ tốt cần thiết cho sản lượng gộp.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVNET
  * *Kí hiệu*: {{< katex >}}N_{c,net}{{< /katex >}}

- **Tờ chạy bìa sau hao hụt biến đổi**
  * *Tờ chạy sản lượng, chưa gồm make-ready.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVRUN
  * *Kí hiệu*: {{< katex >}}N_{c,run}{{< /katex >}}

- **Tờ căn chỉnh bìa**
  * *Make-ready cố định theo khuôn và lượt.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVSET
  * *Kí hiệu*: {{< katex >}}N_{c,set}{{< /katex >}}

- **Tổng tờ giấy bìa tiêu thụ**
  * *Tờ chạy cộng tờ căn chỉnh.*
  * *Đơn vị*: Tờ
  * *Mã*: MATPNB
  * *Kí hiệu*: {{< katex >}}N_c{{< /katex >}}

- **Số bản offset bìa**
  * *Một bản cho mỗi khuôn, màu và mặt.*
  * *Đơn vị*: Bản
  * *Mã*: MATPCB
  * *Kí hiệu*: {{< katex >}}P_c{{< /katex >}}

- **Khổ bình bìa yêu cầu - dài**
  * *Kích thước bố trí bảo thủ gồm bleed, nhíp và thang màu.*
  * *Đơn vị*: cm
  * *Mã*: MATKIBD
  * *Kí hiệu*: {{< katex >}}L_c{{< /katex >}}

- **Khổ bình bìa yêu cầu - rộng**
  * *Kích thước bố trí bảo thủ theo số bìa trên tờ.*
  * *Đơn vị*: cm
  * *Mã*: MATKIBR
  * *Kí hiệu*: {{< katex >}}W_c{{< /katex >}}

- **Bìa vừa tờ chạy**
  * *1 nếu khổ bình vừa tờ chạy ở ít nhất một hướng xoay.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDC
  * *Kí hiệu*: {{< katex >}}V_c{{< /katex >}}

- **Tờ bìa vừa máy**
  * *1 nếu tờ chạy bìa vừa khổ máy ở ít nhất một hướng.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDMC
  * *Kí hiệu*: {{< katex >}}V_{mc}{{< /katex >}}

- **Khối lượng giấy bìa**
  * *Tổng tờ vật lý nhân diện tích tờ chạy và định lượng.*
  * *Đơn vị*: Tấn
  * *Mã*: MATPWB
  * *Kí hiệu*: {{< katex >}}W_c{{< /katex >}}

- **Khối lượng mực bìa**
  * *Tờ-màu-mặt nhân diện tích, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: MATIWB
  * *Kí hiệu*: {{< katex >}}I_c{{< /katex >}}

- **Diện tích màng bìa**
  * *Diện tích tờ bìa tiêu thụ nhân số mặt cán.*
  * *Đơn vị*: m²
  * *Mã*: MATFILM
  * *Kí hiệu*: {{< katex >}}A_f{{< /katex >}}

- **Chiều dài màng chạy**
  * *Tổng chiều dài tờ bìa qua máy cán, nhân số mặt cán.*
  * *Đơn vị*: m
  * *Mã*: MATFILMLEN
  * *Kí hiệu*: {{< katex >}}l_f{{< /katex >}}

## Thông tin tính toán ruột
**Thông tin tín toán ruôt**

- **Số trang ruột sản xuất**
  * *Số trang ruột sau khi bù đủ tay sách.*
  * *Đơn vị*: Trang
  * *Mã*: MATPRODPG
  * *Kí hiệu*: {{< katex >}}p_{prod}{{< /katex >}}

- **Số trang trắng bù tay**
  * *Chênh lệch giữa số trang sản xuất và số trang khách hàng.*
  * *Đơn vị*: Trang
  * *Mã*: MATBLANK
  * *Kí hiệu*: {{< katex >}}p_{blank}{{< /katex >}}

- **Số tay sách mỗi cuốn**
  * *Số tay nguyên vẹn sau bù trang trắng.*
  * *Đơn vị*: Tay/Cuốn
  * *Mã*: MATSIG
  * *Kí hiệu*: {{< katex >}}n_s{{< /katex >}}

- **Số khuôn ruột**
  * *Mỗi tay sách cần một khuôn bình riêng.*
  * *Đơn vị*: Khuôn
  * *Mã*: MATINFORM
  * *Kí hiệu*: {{< katex >}}F_t{{< /katex >}}

- **Số lượt màu ruột**
  * *Số lần chạy để đủ màu theo số đơn vị in của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATINCP
  * *Kí hiệu*: {{< katex >}}r_{t,color}{{< /katex >}}

- **Số lượt mặt ruột**
  * *Số lần chạy để đủ mặt theo khả năng trở mặt của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATINSP
  * *Kí hiệu*: {{< katex >}}r_{t,side}{{< /katex >}}

- **Tổng lượt chạy ruột mỗi khuôn**
  * *Tích lượt màu và lượt mặt.*
  * *Đơn vị*: Lượt/Khuôn
  * *Mã*: MATINPASS
  * *Kí hiệu*: {{< katex >}}r_t{{< /katex >}}

- **Tờ ruột tốt tối thiểu**
  * *Một tờ cho mỗi tay của mỗi khối ruột.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINNET
  * *Kí hiệu*: {{< katex >}}N_{t,net}{{< /katex >}}

- **Tờ chạy ruột sau hao hụt biến đổi**
  * *Tờ chạy sản lượng, chưa gồm make-ready.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINRUN
  * *Kí hiệu*: {{< katex >}}N_{t,run}{{< /katex >}}

- **Tờ căn chỉnh ruột**
  * *Make-ready cố định theo khuôn và lượt.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINSET
  * *Kí hiệu*: {{< katex >}}N_{t,set}{{< /katex >}}

- **Tổng tờ giấy ruột tiêu thụ**
  * *Tờ chạy cộng tờ căn chỉnh.*
  * *Đơn vị*: Tờ
  * *Mã*: MATPNR
  * *Kí hiệu*: {{< katex >}}N_t{{< /katex >}}

- **Số bản offset ruột**
  * *Một bản cho mỗi khuôn, màu và mặt.*
  * *Đơn vị*: Bản
  * *Mã*: MATPCR
  * *Kí hiệu*: {{< katex >}}P_t{{< /katex >}}

- **Khổ bình ruột yêu cầu - dài**
  * *Grid trang trên một mặt tờ, có bleed, nhíp và thang màu.*
  * *Đơn vị*: cm
  * *Mã*: MATKIRD
  * *Kí hiệu*: {{< katex >}}L_t{{< /katex >}}

- **Khổ bình ruột yêu cầu - rộng**
  * *Grid trang trên một mặt tờ theo kiểu bình.*
  * *Đơn vị*: cm
  * *Mã*: MATKIRR
  * *Kí hiệu*: {{< katex >}}W_t{{< /katex >}}

- **Ruột vừa tờ chạy**
  * *1 nếu khổ bình vừa tờ chạy ở ít nhất một hướng xoay.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDT
  * *Kí hiệu*: {{< katex >}}V_t{{< /katex >}}

- **Tờ ruột vừa máy**
  * *1 nếu tờ chạy ruột vừa khổ máy ở ít nhất một hướng.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDMT
  * *Kí hiệu*: {{< katex >}}V_{mt}{{< /katex >}}

- **Khối lượng giấy ruột**
  * *Tổng tờ vật lý nhân diện tích tờ chạy và định lượng.*
  * *Đơn vị*: Tấn
  * *Mã*: MATPWR
  * *Kí hiệu*: {{< katex >}}W_t{{< /katex >}}

- **Khối lượng mực ruột**
  * *Tờ-màu-mặt nhân diện tích, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: MATIWR
  * *Kí hiệu*: {{< katex >}}I_t{{< /katex >}}

## Thông tin tính toán tổng
**Thông tin tín toán tổng**

- **Số khối ruột cần sản xuất**
  * *Sản lượng gộp đã bù hao hụt thành phẩm.*
  * *Đơn vị*: Cuốn
  * *Mã*: MATGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}

- **Chi phí giấy**
  * *Chi phí giấy bìa và ruột theo khối lượng riêng.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCG
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}

- **Chi phí vật tư bản**
  * *Số bản nhân đúng diện tích bản tương ứng.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCBI
  * *Kí hiệu*: {{< katex >}}C_{plate}{{< /katex >}}

- **Chi phí mực**
  * *Khối lượng mực nhân đơn giá; không nhân lại số bản.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCMI
  * *Kí hiệu*: {{< katex >}}C_{ink}{{< /katex >}}

- **Chi phí màng**
  * *Diện tích màng theo m² nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCMB
  * *Kí hiệu*: {{< katex >}}C_f{{< /katex >}}

- **Chi phí chế bản**
  * *Chi phí dịch vụ trên tổng số bản offset.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCCB
  * *Kí hiệu*: {{< katex >}}C_{prep}{{< /katex >}}

- **Chi phí chạy máy in**
  * *Setup theo khuôn-lượt cộng chi phí biến đổi theo lượt tờ.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCPR
  * *Kí hiệu*: {{< katex >}}C_{press}{{< /katex >}}

- **Chi phí hoàn thiện**
  * *Phần theo tay sách cộng phần theo cuốn trên sản lượng gộp.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCGC
  * *Kí hiệu*: {{< katex >}}C_{finish}{{< /katex >}}

- **Chi phí đơn hàng**
  * *Tổng vật tư, chế bản, chạy máy, hoàn thiện và khoản khác.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCDH
  * *Kí hiệu*: {{< katex >}}C_{order}{{< /katex >}}

- **Chi phí tính toán mỗi cuốn giao**
  * *Chi phí đơn hàng chia số cuốn tốt cần giao; chưa phải báo giá bán.*
  * *Đơn vị*: VNĐ/Cuốn
  * *Mã*: MATPRSIN
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}

## Thông tin tính toán khác
**Thông tin tín toán khác**

- **Tổng số trang khách hàng**
  * *Tổng số trang bìa và ruột khách hàng.*
  * *Đơn vị*: Trang
  * *Mã*: MATSNP
  * *Kí hiệu*: {{< katex >}}p{{< /katex >}}

- **Độ dày khối ruột tại gáy**
  * *Số lá nhân caliper đo được và hệ số hiệu chỉnh sau khâu/nén.*
  * *Đơn vị*: cm
  * *Mã*: MATGS
  * *Kí hiệu*: {{< katex >}}s{{< /katex >}}

- **Gáy trong giới hạn máy đóng cuốn**
  * *1 nếu độ dày gáy nằm trong giới hạn cấu hình.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDS
  * *Kí hiệu*: {{< katex >}}V_s{{< /katex >}}



