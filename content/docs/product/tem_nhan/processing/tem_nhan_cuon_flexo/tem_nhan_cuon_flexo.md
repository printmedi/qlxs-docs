---
weight: 1
type: docs
title: Công Thức
url: /tem_nhan/tem_nhan_cuon_flexo
---

# Tem nhãn cuộn flexo

Tem tự dính hình chữ nhật in flexo trên web, bế inline và chia cuộn offline.
Engine sinh candidate khổ cuộn/repeat/số tem ngang-quanh; generator chỉ kiểm tra
và tính một candidate. Model chưa factory-calibrated và không áp dụng cho shrink
sleeve, IML, linerless, tem nhiều lớp hoặc in kỹ thuật số cuộn.


# Thông Tin Tính Toán

## Tính Toán
### Tính Toán Nguyên Vật Liệu
- **Số tem mục tiêu trước hoàn thiện**
  * *Sản lượng giao đã nâng theo hao hụt thành phẩm riêng.*
  * *Đơn vị*: Tem
  * *Mã*: TMCGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q / (1 - w_f)}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng tem cần giao (Tem)<br>
{{< katex >}}w_f{{< /katex >}}: Tỷ lệ hao hụt thành phẩm tem (Tỷ lệ)<br>

  {{< /details >}}
- **Số tem mỗi repeat**
  * *Tích số tem ngang và số tem quanh repeat.*
  * *Đơn vị*: Tem/Repeat
  * *Mã*: TMCPERREPEAT
  * *Kí hiệu*: {{< katex >}}N_R{{< /katex >}}
  * *Công thức* :{{< katex >}}n_x * n_y{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}n_x{{< /katex >}}: Số tem ngang (Tem)<br>
{{< katex >}}n_y{{< /katex >}}: Số tem quanh repeat (Tem)<br>

  {{< /details >}}
- **Số repeat cần chạy**
  * *Số repeat nguyên cần chạy để đạt sản lượng mục tiêu trước hao hụt.*
  * *Đơn vị*: Repeat
  * *Mã*: TMCREPEATS
  * *Kí hiệu*: {{< katex >}}N_{repeat}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q_g / N_R}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số tem mục tiêu trước hoàn thiện (Tem)<br>
{{< katex >}}N_R{{< /katex >}}: Số tem mỗi repeat (Tem/Repeat)<br>

  {{< /details >}}
- **Tổng tem bố trí được**
  * *Số repeat nhân số tem trên repeat trước loại thành phẩm.*
  * *Đơn vị*: Tem
  * *Mã*: TMCPRODUCED
  * *Kí hiệu*: {{< katex >}}Q_p{{< /katex >}}
  * *Công thức* :{{< katex >}}N_{repeat} * N_R{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{repeat}{{< /katex >}}: Số repeat cần chạy (Repeat)<br>
{{< katex >}}N_R{{< /katex >}}: Số tem mỗi repeat (Tem/Repeat)<br>

  {{< /details >}}
- **Số tem sản xuất vượt lượng giao**
  * *Chênh lệch hình học giữa tổng tem bố trí và số lượng khách hàng yêu cầu; gồm phần dự phòng hao hụt.*
  * *Đơn vị*: Tem
  * *Mã*: TMCOVERRUN
  * *Kí hiệu*: {{< katex >}}Q_o{{< /katex >}}
  * *Công thức* :{{< katex >}}Q_p - Q{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_p{{< /katex >}}: Tổng tem bố trí được (Tem)<br>
{{< katex >}}Q{{< /katex >}}: Số lượng tem cần giao (Tem)<br>

  {{< /details >}}
- **Chiều dài web thuần**
  * *Số repeat nhân repeat, chưa gồm hao hụt chạy và mét setup.*
  * *Đơn vị*: m
  * *Mã*: TMCNETLEN
  * *Kí hiệu*: {{< katex >}}L_n{{< /katex >}}
  * *Công thức* :{{< katex >}}N_{repeat} * R * 0.001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{repeat}{{< /katex >}}: Số repeat cần chạy (Repeat)<br>
{{< katex >}}R{{< /katex >}}: Chiều dài repeat (mm)<br>

  {{< /details >}}
- **Tổng chiều dài web cần chạy**
  * *Chiều dài thuần đã bù hao hụt chạy, sau đó cộng mét setup cố định.*
  * *Đơn vị*: m
  * *Mã*: TMCTOTALLEN
  * *Kí hiệu*: {{< katex >}}L_t{{< /katex >}}
  * *Công thức* :{{< katex >}}L_n / (1 - w_r) + L_{setup}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_n{{< /katex >}}: Chiều dài web thuần (m)<br>
{{< katex >}}w_r{{< /katex >}}: Tỷ lệ hao hụt chạy web (Tỷ lệ)<br>
{{< katex >}}L_{setup}{{< /katex >}}: Mét vật liệu setup cố định (m)<br>

  {{< /details >}}
- **Tổng diện tích vật liệu tem**
  * *Toàn bộ web mua/chạy gồm setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: TMCAREA
  * *Kí hiệu*: {{< katex >}}A_t{{< /katex >}}
  * *Công thức* :{{< katex >}}L_t * W * 0.001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_t{{< /katex >}}: Tổng chiều dài web cần chạy (m)<br>
{{< katex >}}W{{< /katex >}}: Khổ cuộn chạy (mm)<br>

  {{< /details >}}
- **Diện tích tem thành phẩm giao**
  * *Diện tích hình chữ nhật của lượng tem giao, không gồm gap và liner xung quanh.*
  * *Đơn vị*: m²
  * *Mã*: TMCDELIVEREDAREA
  * *Kí hiệu*: {{< katex >}}A_l{{< /katex >}}
  * *Công thức* :{{< katex >}}Q * w * h * 0.000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng tem cần giao (Tem)<br>
{{< katex >}}w{{< /katex >}}: Chiều rộng tem (mm)<br>
{{< katex >}}h{{< /katex >}}: Chiều dài tem (mm)<br>

  {{< /details >}}
- **Diện tích vật liệu ngoài tem giao**
  * *Tổng diện tích web trừ diện tích hình học tem giao; gồm liner giữa tem, biên, setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: TMCWASTEAREA
  * *Kí hiệu*: {{< katex >}}A_w{{< /katex >}}
  * *Công thức* :{{< katex >}}A_t - A_l{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_t{{< /katex >}}: Tổng diện tích vật liệu tem (m²)<br>
{{< katex >}}A_l{{< /katex >}}: Diện tích tem thành phẩm giao (m²)<br>

  {{< /details >}}
- **Tỷ lệ diện tích ngoài tem giao**
  * *Phần diện tích web không trở thành diện tích hình học tem giao.*
  * *Đơn vị*: %
  * *Mã*: TMCWASTEPCT
  * *Kí hiệu*: {{< katex >}}U_w{{< /katex >}}
  * *Công thức* :{{< katex >}}A_w * 100 / A_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_w{{< /katex >}}: Diện tích vật liệu ngoài tem giao (m²)<br>
{{< katex >}}A_t{{< /katex >}}: Tổng diện tích vật liệu tem (m²)<br>

  {{< /details >}}
- **Tổng diện tích bản flexo**
  * *Diện tích khổ cuộn nhân repeat và số màu; bootstrap hình học, production dùng kích thước bản thực tế.*
  * *Đơn vị*: m²
  * *Mã*: TMCPLATEAREA
  * *Kí hiệu*: {{< katex >}}A_p{{< /katex >}}
  * *Công thức* :{{< katex >}}W * R * c * 0.000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}W{{< /katex >}}: Khổ cuộn chạy (mm)<br>
{{< katex >}}R{{< /katex >}}: Chiều dài repeat (mm)<br>
{{< katex >}}c{{< /katex >}}: Số màu in flexo (Màu)<br>

  {{< /details >}}
- **Khối lượng mực flexo**
  * *Diện tích web nhân số màu, độ phủ trung bình và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: TMCINKKG
  * *Kí hiệu*: {{< katex >}}M_i{{< /katex >}}
  * *Công thức* :{{< katex >}}A_t * c * a * 0.01 * f_{ink} * 0.001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_t{{< /katex >}}: Tổng diện tích vật liệu tem (m²)<br>
{{< katex >}}c{{< /katex >}}: Số màu in flexo (Màu)<br>
{{< katex >}}a{{< /katex >}}: Độ phủ trung bình mỗi màu (%)<br>
{{< katex >}}f_{ink}{{< /katex >}}: Định mức màng mực flexo tại 100% phủ (g/m²)<br>

  {{< /details >}}
- **Chi phí vật liệu tem**
  * *Tổng diện tích web nhân đơn giá construction.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTSTOCK
  * *Kí hiệu*: {{< katex >}}C_s{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{A_t * P_{stock}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_t{{< /katex >}}: Tổng diện tích vật liệu tem (m²)<br>
{{< katex >}}P_{stock}{{< /katex >}}: Đơn giá vật liệu tem tự dính (VNĐ/m²)<br>

  {{< /details >}}
- **Chi phí bản flexo**
  * *Diện tích bản hình học nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTPLATE
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{A_p * P_{plate}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_p{{< /katex >}}: Tổng diện tích bản flexo (m²)<br>
{{< katex >}}P_{plate}{{< /katex >}}: Đơn giá bản flexo theo diện tích (VNĐ/m²)<br>

  {{< /details >}}
- **Chi phí mực flexo**
  * *Khối lượng mực nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTINK
  * *Kí hiệu*: {{< katex >}}C_i{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{M_i * P_{ink}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}M_i{{< /katex >}}: Khối lượng mực flexo (kg)<br>
{{< katex >}}P_{ink}{{< /katex >}}: Đơn giá mực flexo (VNĐ/kg)<br>

  {{< /details >}}
- **Chi phí chạy máy flexo**
  * *Setup cố định cộng chi phí theo mét web thực chạy; bế inline không cộng lại mét chạy.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTPRESS
  * *Kí hiệu*: {{< katex >}}C_{press}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{C_{setup} + L_t * C_{run,m}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_{setup}{{< /katex >}}: Chi phí setup máy flexo (VNĐ)<br>
{{< katex >}}L_t{{< /katex >}}: Tổng chiều dài web cần chạy (m)<br>
{{< katex >}}C_{run,m}{{< /katex >}}: Chi phí chạy máy flexo theo mét (VNĐ/m)<br>

  {{< /details >}}
- **Chi phí chia cuộn**
  * *Chi phí chia/rewind offline theo mét web.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTSLIT
  * *Kí hiệu*: {{< katex >}}C_{slit}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{L_t * C_{slit,m}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_t{{< /katex >}}: Tổng chiều dài web cần chạy (m)<br>
{{< katex >}}C_{slit,m}{{< /katex >}}: Chi phí chia cuộn theo mét (VNĐ/m)<br>

  {{< /details >}}
- **Chi phí đơn hàng**
  * *Tổng vật liệu, bản, mực, chạy máy, chia cuộn và chi phí khác.*
  * *Đơn vị*: VNĐ
  * *Mã*: TMCCOSTORDER
  * *Kí hiệu*: {{< katex >}}C_o{{< /katex >}}
  * *Công thức* :{{< katex >}}C_s + C_p + C_i + C_{press} + C_{slit} + C_{other}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_s{{< /katex >}}: Chi phí vật liệu tem (VNĐ)<br>
{{< katex >}}C_p{{< /katex >}}: Chi phí bản flexo (VNĐ)<br>
{{< katex >}}C_i{{< /katex >}}: Chi phí mực flexo (VNĐ)<br>
{{< katex >}}C_{press}{{< /katex >}}: Chi phí chạy máy flexo (VNĐ)<br>
{{< katex >}}C_{slit}{{< /katex >}}: Chi phí chia cuộn (VNĐ)<br>
{{< katex >}}C_{other}{{< /katex >}}: Chi phí đơn hàng khác (VNĐ)<br>

  {{< /details >}}
- **Đơn giá tính toán mỗi tem**
  * *Chi phí đơn hàng chia số tem tốt cần giao; chưa phải giá bán.*
  * *Đơn vị*: VNĐ/Tem
  * *Mã*: TMCCOSTUNIT
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{C_o / Q}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_o{{< /katex >}}: Chi phí đơn hàng (VNĐ)<br>
{{< katex >}}Q{{< /katex >}}: Số lượng tem cần giao (Tem)<br>

  {{< /details >}}
- **Số cuộn thành phẩm**
  * *Số cuộn giao khách; khi không giới hạn chia nhỏ, mỗi lane ngang tạo một cuộn.*
  * *Đơn vị*: Cuộn
  * *Mã*: TMCROLLS
  * *Kí hiệu*: {{< katex >}}N_{roll}{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}q_{roll}{{< /katex >}} bằng [•  0  	]: {{< katex >}}n_x{{< /katex >}}
	* Ngoài ra: {{< katex >}}\lceil{Q / q_{roll}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng tem cần giao (Tem)<br>
{{< katex >}}q_{roll}{{< /katex >}}: Số tem tối đa mỗi cuộn thành phẩm (Tem/Cuộn)<br>
{{< katex >}}n_x{{< /katex >}}: Số tem ngang (Tem)<br>

  {{< /details >}}
- **Số tem ngang/quanh hợp lệ**
  * *1 nếu hai số lượng là số nguyên dương.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDCOUNT
  * *Kí hiệu*: {{< katex >}}V_n{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}n_x{{< /katex >}} thỏa mãn {{< katex >}}(n_x >= 1 && n_y >= 1 && \lceil{n_x}\rceil == n_x && \lceil{n_y}\rceil == n_y){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}n_x{{< /katex >}}: Số tem ngang (Tem)<br>
{{< katex >}}n_y{{< /katex >}}: Số tem quanh repeat (Tem)<br>

  {{< /details >}}
- **Bố trí tem vừa khổ cuộn và repeat**
  * *1 nếu candidate vừa theo hướng gốc hoặc hướng hoán đổi dài-rộng; generator không nhận input hướng xoay riêng.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDLAYOUT
  * *Kí hiệu*: {{< katex >}}V_l{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}W{{< /katex >}} thỏa mãn {{< katex >}}((((n_x * w + (n_x - 1) * g_x + 2 * e) <= W) && ((n_x * w + (n_x - 1) * g_x) <= P_{max}) && (n_y * (h + g_y) <= R)) || (((n_x * h + (n_x - 1) * g_x + 2 * e) <= W) && ((n_x * h + (n_x - 1) * g_x) <= P_{max}) && (n_y * (w + g_y) <= R))){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}W{{< /katex >}}: Khổ cuộn chạy (mm)<br>
{{< katex >}}n_x{{< /katex >}}: Số tem ngang (Tem)<br>
{{< katex >}}w{{< /katex >}}: Chiều rộng tem (mm)<br>
{{< katex >}}g_x{{< /katex >}}: Khoảng cách tem ngang (mm)<br>
{{< katex >}}e{{< /katex >}}: Lề biên cuộn mỗi bên (mm)<br>
{{< katex >}}P_{max}{{< /katex >}}: Khổ in hữu dụng tối đa (mm)<br>
{{< katex >}}n_y{{< /katex >}}: Số tem quanh repeat (Tem)<br>
{{< katex >}}h{{< /katex >}}: Chiều dài tem (mm)<br>
{{< katex >}}g_y{{< /katex >}}: Khoảng cách tem dọc (mm)<br>
{{< katex >}}R{{< /katex >}}: Chiều dài repeat (mm)<br>

  {{< /details >}}
- **Khổ cuộn trong giới hạn máy**
  * *1 nếu khổ cuộn candidate không vượt khổ web tối đa của máy.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDWEB
  * *Kí hiệu*: {{< katex >}}V_W{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}W{{< /katex >}} thỏa mãn {{< katex >}}(W <= WMAX){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}W{{< /katex >}}: Khổ cuộn chạy (mm)<br>
{{< katex >}}W_{max}{{< /katex >}}: Khổ web tối đa của máy (mm)<br>

  {{< /details >}}
- **Repeat trong giới hạn in và bế**
  * *1 nếu repeat candidate nằm đồng thời trong khoảng của cụm in và cụm bế inline.*
  * *Đơn vị*: Boolean
  * *Mã*: TMCVALIDREPEAT
  * *Kí hiệu*: {{< katex >}}V_R{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}R{{< /katex >}} thỏa mãn {{< katex >}}(R >= R_{p,min} && R <= R_{p,max} && R >= R_{d,min} && R <= R_{d,max}){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}R{{< /katex >}}: Chiều dài repeat (mm)<br>
{{< katex >}}R_{p,min}{{< /katex >}}: Repeat in tối thiểu (mm)<br>
{{< katex >}}R_{p,max}{{< /katex >}}: Repeat in tối đa (mm)<br>
{{< katex >}}R_{d,min}{{< /katex >}}: Repeat bế tối thiểu (mm)<br>
{{< katex >}}R_{d,max}{{< /katex >}}: Repeat bế tối đa (mm)<br>

  {{< /details >}}
### Tính Toán Thời Gian
- **Tổng thời gian chế bản thuộc model**
  * *V1 chưa định lượng workflow artwork/RIP/làm bản riêng; trả 0 minh bạch thay vì dùng công thức Sách.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTPREPRESS
  * *Kí hiệu*: {{< katex >}}T_{pre}{{< /katex >}}
- **In flexo và bế inline**
  * *Một stage tích hợp theo tổng mét web; không cộng bế inline lần hai.*
  * *Đơn vị*: Phút
  * *Mã*: TCCPRINT
  * *Kí hiệu*: {{< katex >}}T_p{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{L_t / v_p + T_{p,setup}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_t{{< /katex >}}: Tổng chiều dài web cần chạy (m)<br>
{{< katex >}}v_p{{< /katex >}}: Tốc độ planning máy flexo cuộn (m/Phút)<br>
{{< katex >}}T_{p,setup}{{< /katex >}}: Thời gian setup máy flexo cuộn (Phút)<br>

  {{< /details >}}
- **Tổng thời gian in**
  * *Tổng thời gian chiếm dụng máy in cuộn trong model.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTPRINT
  * *Kí hiệu*: {{< katex >}}T_{print}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_p{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_p{{< /katex >}}: In flexo và bế inline (Phút)<br>

  {{< /details >}}
- **Chia cuộn tem**
  * *Thời gian máy chia/kiểm tra/rewind offline theo tổng mét web.*
  * *Đơn vị*: Phút
  * *Mã*: TCCSLIT
  * *Kí hiệu*: {{< katex >}}T_s{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{L_t / v_s + T_{s,setup}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_t{{< /katex >}}: Tổng chiều dài web cần chạy (m)<br>
{{< katex >}}v_s{{< /katex >}}: Tốc độ planning chia cuộn (m/Phút)<br>
{{< katex >}}T_{s,setup}{{< /katex >}}: Thời gian setup máy chia cuộn (Phút)<br>

  {{< /details >}}
- **Tổng thời gian hoàn thiện**
  * *Tổng stage hoàn thiện được processing bật.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTCOMP
  * *Kí hiệu*: {{< katex >}}T_{finish}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_s{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_s{{< /katex >}}: Chia cuộn tem (Phút)<br>

  {{< /details >}}
- **Tổng thời gian sản xuất**
  * *Tổng thời gian chế bản, in và hoàn thiện trong phạm vi model.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTTOTAL
  * *Kí hiệu*: {{< katex >}}T_{total}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_{pre} + T_{print} + T_{finish}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_{pre}{{< /katex >}}: Tổng thời gian chế bản thuộc model (Phút)<br>
{{< katex >}}T_{print}{{< /katex >}}: Tổng thời gian in (Phút)<br>
{{< katex >}}T_{finish}{{< /katex >}}: Tổng thời gian hoàn thiện (Phút)<br>

  {{< /details >}}



