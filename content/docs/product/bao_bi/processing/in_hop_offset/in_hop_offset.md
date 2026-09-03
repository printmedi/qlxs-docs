---
weight: 1
type: docs
title: Công Thức
url: /bao_bi/in_hop_offset
---

# In hộp offset tờ rời

Engine dựng khuôn hộp theo profile, dùng u-nesting để tìm số hộp trên tờ và
gửi một candidate scalar. Generator tính candidate đó qua chế bản, pha cắt,
in offset, bế/cấn/tách phế, gấp-dán và đóng gói hộp phẳng.


# Thông Tin Tính Toán

## Tính Toán
### Tính Toán Nguyên Vật Liệu
- **Số hộp mục tiêu trước hao hụt thành phẩm**
  * *Sản lượng giao nâng riêng theo hao hụt sau in.*
  * *Đơn vị*: Hộp
  * *Mã*: BBCGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q / (1 - w_f)}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng hộp cần giao (Hộp)<br>
{{< katex >}}w_f{{< /katex >}}: Tỷ lệ hao hụt thành phẩm hộp (Tỷ lệ)<br>

  {{< /details >}}
- **Số tờ tốt cần có**
  * *Số hộp mục tiêu chia cho số hộp trên tờ.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCGOODSHEETS
  * *Kí hiệu*: {{< katex >}}N_g{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q_g / N_s}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số hộp mục tiêu trước hao hụt thành phẩm (Hộp)<br>
{{< katex >}}N_s{{< /katex >}}: Số hộp trên một tờ (Hộp/Tờ)<br>

  {{< /details >}}
- **Số tờ cần chạy trước setup**
  * *Tờ tốt đã bù hao hụt biến đổi khi chạy in.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCRUNSHEETS
  * *Kí hiệu*: {{< katex >}}N_r{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_g / (1 - w_r)}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_g{{< /katex >}}: Số tờ tốt cần có (Tờ)<br>
{{< katex >}}w_r{{< /katex >}}: Tỷ lệ hao hụt chạy in hộp (Tỷ lệ)<br>

  {{< /details >}}
- **Tổng số tờ chạy**
  * *Tờ chạy biến đổi cộng tờ setup cố định.*
  * *Đơn vị*: Tờ
  * *Mã*: BBCTOTALSHEETS
  * *Kí hiệu*: {{< katex >}}N_t{{< /katex >}}
  * *Công thức* :{{< katex >}}N_r + N_{setup}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_r{{< /katex >}}: Số tờ cần chạy trước setup (Tờ)<br>
{{< katex >}}N_{setup}{{< /katex >}}: Số tờ căn chỉnh máy in hộp (Tờ)<br>

  {{< /details >}}
- **Số hộp bố trí vượt lượng giao**
  * *Sức chứa hình học của số tờ tốt trừ lượng giao.*
  * *Đơn vị*: Hộp
  * *Mã*: BBCOVERRUN
  * *Kí hiệu*: {{< katex >}}Q_o{{< /katex >}}
  * *Công thức* :{{< katex >}}N_g * N_s - Q{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_g{{< /katex >}}: Số tờ tốt cần có (Tờ)<br>
{{< katex >}}N_s{{< /katex >}}: Số hộp trên một tờ (Hộp/Tờ)<br>
{{< katex >}}Q{{< /katex >}}: Số lượng hộp cần giao (Hộp)<br>

  {{< /details >}}
- **Tổng diện tích giấy chạy**
  * *Toàn bộ tờ chạy gồm setup và hao hụt.*
  * *Đơn vị*: m²
  * *Mã*: BBCSHEETAREA
  * *Kí hiệu*: {{< katex >}}A_s{{< /katex >}}
  * *Công thức* :{{< katex >}}N_t * S_L * S_W * 0.0001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng số tờ chạy (Tờ)<br>
{{< katex >}}S_L{{< /katex >}}: Khổ tờ chạy - dài (cm)<br>
{{< katex >}}S_W{{< /katex >}}: Khổ tờ chạy - rộng (cm)<br>

  {{< /details >}}
- **Khối lượng giấy hộp**
  * *Diện tích giấy chạy nhân định lượng.*
  * *Đơn vị*: kg
  * *Mã*: BBCPAPERKG
  * *Kí hiệu*: {{< katex >}}M_s{{< /katex >}}
  * *Công thức* :{{< katex >}}A_s * G * 0.001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_s{{< /katex >}}: Tổng diện tích giấy chạy (m²)<br>
{{< katex >}}G{{< /katex >}}: Định lượng giấy hộp (g/m²)<br>

  {{< /details >}}
- **Hiệu suất diện tích nesting**
  * *Tổng diện tích polygon hộp trên một tờ chia diện tích tờ vật lý.*
  * *Đơn vị*: %
  * *Mã*: BBCUTIL
  * *Kí hiệu*: {{< katex >}}U{{< /katex >}}
  * *Công thức* :{{< katex >}}N_s * A_d * 100 / (S_L * S_W * 100){{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_s{{< /katex >}}: Số hộp trên một tờ (Hộp/Tờ)<br>
{{< katex >}}A_d{{< /katex >}}: Diện tích khuôn phẳng một hộp (mm²)<br>
{{< katex >}}S_L{{< /katex >}}: Khổ tờ chạy - dài (cm)<br>
{{< katex >}}S_W{{< /katex >}}: Khổ tờ chạy - rộng (cm)<br>

  {{< /details >}}
- **Số bản in hộp**
  * *Một bản cho mỗi màu và mỗi mặt in.*
  * *Đơn vị*: Bản
  * *Mã*: BBCPLATES
  * *Kí hiệu*: {{< katex >}}N_p{{< /katex >}}
  * *Công thức* :{{< katex >}}C * D{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C{{< /katex >}}: Số màu in hộp (Màu)<br>
{{< katex >}}D{{< /katex >}}: Số mặt in hộp (Mặt)<br>

  {{< /details >}}
- **Tổng lượt chạy máy in**
  * *Số pass màu nhân số pass mặt theo khả năng máy.*
  * *Đơn vị*: Lượt
  * *Mã*: BBCRUNS
  * *Kí hiệu*: {{< katex >}}R{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{C / C_m}\rceil * \lceil{D / D_m}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C{{< /katex >}}: Số màu in hộp (Màu)<br>
{{< katex >}}C_m{{< /katex >}}: Số màu máy in hỗ trợ (Màu)<br>
{{< katex >}}D{{< /katex >}}: Số mặt in hộp (Mặt)<br>
{{< katex >}}D_m{{< /katex >}}: Số mặt máy in hỗ trợ (Mặt)<br>

  {{< /details >}}
- **Khối lượng mực offset**
  * *Diện tích tờ chạy nhân màu, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: BBCINKKG
  * *Kí hiệu*: {{< katex >}}M_i{{< /katex >}}
  * *Công thức* :{{< katex >}}A_s * C * a * 0.01 * f_i * 0.001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_s{{< /katex >}}: Tổng diện tích giấy chạy (m²)<br>
{{< katex >}}C{{< /katex >}}: Số màu in hộp (Màu)<br>
{{< katex >}}a{{< /katex >}}: Độ phủ trung bình mỗi màu (%)<br>
{{< katex >}}f_i{{< /katex >}}: Định mức màng mực offset tại 100% phủ (g/m²)<br>

  {{< /details >}}
- **Số hộp trên tờ hợp lệ**
  * *1 khi số hộp/tờ là số nguyên dương.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDCOUNT
  * *Kí hiệu*: {{< katex >}}V_n{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}N_s{{< /katex >}} thỏa mãn {{< katex >}}(N_s >= 1 && \lceil{N_s}\rceil == N_s){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_s{{< /katex >}}: Số hộp trên một tờ (Hộp/Tờ)<br>

  {{< /details >}}
- **Diện tích nesting hợp lệ**
  * *Kiểm tra bảo thủ rằng tổng diện tích polygon không vượt diện tích tờ; engine chịu trách nhiệm kiểm tra va chạm thật.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDAREA
  * *Kí hiệu*: {{< katex >}}V_l{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}A_d{{< /katex >}} thỏa mãn {{< katex >}}(N_s * A_d <= S_L * S_W * 100){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_d{{< /katex >}}: Diện tích khuôn phẳng một hộp (mm²)<br>
{{< katex >}}N_s{{< /katex >}}: Số hộp trên một tờ (Hộp/Tờ)<br>
{{< katex >}}S_L{{< /katex >}}: Khổ tờ chạy - dài (cm)<br>
{{< katex >}}S_W{{< /katex >}}: Khổ tờ chạy - rộng (cm)<br>

  {{< /details >}}
- **Tờ hộp vừa máy in**
  * *Cho phép xoay cả tờ 90 độ khi so với khổ máy.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDMACHINE
  * *Kí hiệu*: {{< katex >}}V_m{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}S_L{{< /katex >}} thỏa mãn {{< katex >}}(((S_L <= M_L) && (S_W <= M_W)) || ((S_L <= M_W) && (S_W <= M_L))){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}S_L{{< /katex >}}: Khổ tờ chạy - dài (cm)<br>
{{< katex >}}M_L{{< /katex >}}: Khổ máy in - dài (cm)<br>
{{< katex >}}S_W{{< /katex >}}: Khổ tờ chạy - rộng (cm)<br>
{{< katex >}}M_W{{< /katex >}}: Khổ máy in - rộng (cm)<br>

  {{< /details >}}
- **Tờ hộp vừa máy bế**
  * *Cho phép xoay cả tờ 90 độ khi so với khổ máy bế đã chọn.*
  * *Đơn vị*: Boolean
  * *Mã*: BBCVALIDDIECUT
  * *Kí hiệu*: {{< katex >}}V_d{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}S_L{{< /katex >}} thỏa mãn {{< katex >}}(((S_L <= D_L) && (S_W <= D_W)) || ((S_L <= D_W) && (S_W <= D_L))){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}S_L{{< /katex >}}: Khổ tờ chạy - dài (cm)<br>
{{< katex >}}D_L{{< /katex >}}: Khổ máy bế - dài (cm)<br>
{{< katex >}}S_W{{< /katex >}}: Khổ tờ chạy - rộng (cm)<br>
{{< katex >}}D_W{{< /katex >}}: Khổ máy bế - rộng (cm)<br>

  {{< /details >}}
- **Chi phí giấy hộp**
  * *Khối lượng giấy nhân đơn giá theo tấn.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPAPER
  * *Kí hiệu*: {{< katex >}}C_s{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{M_s * P_s / 1000}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}M_s{{< /katex >}}: Khối lượng giấy hộp (kg)<br>
{{< katex >}}P_s{{< /katex >}}: Đơn giá giấy hộp (VNĐ/Tấn)<br>

  {{< /details >}}
- **Chi phí mực hộp**
  * *Khối lượng mực nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTINK
  * *Kí hiệu*: {{< katex >}}C_i{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{M_i * P_i}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}M_i{{< /katex >}}: Khối lượng mực offset (kg)<br>
{{< katex >}}P_i{{< /katex >}}: Đơn giá mực offset (VNĐ/kg)<br>

  {{< /details >}}
- **Chi phí bản offset**
  * *Số bản nhân đơn giá mỗi bản.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPLATE
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_p * P_p}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_p{{< /katex >}}: Số bản in hộp (Bản)<br>
{{< katex >}}P_p{{< /katex >}}: Đơn giá một bản offset (VNĐ/Bản)<br>

  {{< /details >}}
- **Chi phí máy in**
  * *Tổng thời gian in và setup nhân đơn giá giờ máy.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTPRESS
  * *Kí hiệu*: {{< katex >}}C_m{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(T_{run} + T_s) * P_m / 60}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_{run}{{< /katex >}}: Chạy in hộp (Phút)<br>
{{< katex >}}T_s{{< /katex >}}: Căn chỉnh in hộp (Phút)<br>
{{< katex >}}P_m{{< /katex >}}: Đơn giá giờ máy in offset (VNĐ/Giờ)<br>

  {{< /details >}}
- **Chi phí đơn hàng**
  * *Tổng chi phí thuộc phạm vi model in hộp offset.*
  * *Đơn vị*: VNĐ
  * *Mã*: BBCCOSTORDER
  * *Kí hiệu*: {{< katex >}}C_o{{< /katex >}}
  * *Công thức* :{{< katex >}}C_s + C_i + C_p + C_m + C_o{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_s{{< /katex >}}: Chi phí giấy hộp (VNĐ)<br>
{{< katex >}}C_i{{< /katex >}}: Chi phí mực hộp (VNĐ)<br>
{{< katex >}}C_p{{< /katex >}}: Chi phí bản offset (VNĐ)<br>
{{< katex >}}C_m{{< /katex >}}: Chi phí máy in (VNĐ)<br>
{{< katex >}}C_o{{< /katex >}}: Chi phí đơn hàng khác (VNĐ)<br>

  {{< /details >}}
- **Đơn giá tính toán mỗi hộp**
  * *Chi phí đơn hàng chia sản lượng cần giao; chưa phải giá bán.*
  * *Đơn vị*: VNĐ/Hộp
  * *Mã*: BBCCOSTUNIT
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{C_o / Q}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_o{{< /katex >}}: Chi phí đơn hàng (VNĐ)<br>
{{< katex >}}Q{{< /katex >}}: Số lượng hộp cần giao (Hộp)<br>

  {{< /details >}}
### Tính Toán Thời Gian
- **Bình bản hộp**
  * *Bình một form khuôn hộp lên khổ tờ candidate đã chọn.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTIMPOSE
  * *Kí hiệu*: {{< katex >}}T_i{{< /katex >}}
  * *Công thức* :{{< katex >}}t_i{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}t_i{{< /katex >}}: Thời gian bình bản hộp (Phút)<br>

  {{< /details >}}
- **RIP hộp**
  * *Một form hộp cho mỗi mặt in; tốc độ RIP tính theo mặt artwork.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTRIP
  * *Kí hiệu*: {{< katex >}}T_r{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{D / v_r}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}D{{< /katex >}}: Số mặt in hộp (Mặt)<br>
{{< katex >}}v_r{{< /katex >}}: Tốc độ RIP hộp (Mặt/Phút)<br>

  {{< /details >}}
- **Ghi hiện bản hộp**
  * *Mỗi màu trên mỗi mặt cần một bản offset riêng.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPLATE
  * *Kí hiệu*: {{< katex >}}T_p{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_p * t_p}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_p{{< /katex >}}: Số bản in hộp (Bản)<br>
{{< katex >}}t_p{{< /katex >}}: Thời gian ghi hiện mỗi bản hộp (Phút/Bản)<br>

  {{< /details >}}
- **In thử hộp**
  * *Proof một trang cho mỗi mặt artwork, cộng thời gian chuẩn bị thiết bị.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPROOF
  * *Kí hiệu*: {{< katex >}}T_t{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{D / v_t + t_t}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}D{{< /katex >}}: Số mặt in hộp (Mặt)<br>
{{< katex >}}v_t{{< /katex >}}: Tốc độ in thử hộp (Trang/phút)<br>
{{< katex >}}t_t{{< /katex >}}: Thời gian chuẩn bị in thử hộp (Phút)<br>

  {{< /details >}}
- **Tổng thời gian chế bản**
  * *Bình bản, RIP, ghi hiện toàn bộ bản offset và in thử.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPREPRESS
  * *Kí hiệu*: {{< katex >}}T_{pre}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_i + T_r + T_p + T_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_i{{< /katex >}}: Bình bản hộp (Phút)<br>
{{< katex >}}T_r{{< /katex >}}: RIP hộp (Phút)<br>
{{< katex >}}T_p{{< /katex >}}: Ghi hiện bản hộp (Phút)<br>
{{< katex >}}T_t{{< /katex >}}: In thử hộp (Phút)<br>

  {{< /details >}}
- **Pha cắt tờ hộp**
  * *Chia tổng tờ cần chạy thành chồng theo caliper rồi nhân số nhát cắt mỗi chồng; bằng 0 nếu tờ đã đúng khổ.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRECUT
  * *Kí hiệu*: {{< katex >}}T_c{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{(N_t * t * 0.0001) / h_c}\rceil * N_c * t_c}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng số tờ chạy (Tờ)<br>
{{< katex >}}t{{< /katex >}}: Độ dày giấy hộp (µm)<br>
{{< katex >}}h_c{{< /katex >}}: Chiều cao chồng pha cắt hộp (CM)<br>
{{< katex >}}N_c{{< /katex >}}: Số nhát pha cắt mỗi chồng (Nhát/Chồng)<br>
{{< katex >}}t_c{{< /katex >}}: Thời gian một nhát pha cắt hộp (Phút/Chồng)<br>

  {{< /details >}}
- **Chạy in hộp**
  * *Tổng tờ chạy nhân số lượt pass theo khả năng máy.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRINT
  * *Kí hiệu*: {{< katex >}}T_{run}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_t * R * 60 / v}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng số tờ chạy (Tờ)<br>
{{< katex >}}R{{< /katex >}}: Tổng lượt chạy máy in (Lượt)<br>
{{< katex >}}v{{< /katex >}}: Tốc độ planning máy in hộp (Tờ/Giờ)<br>

  {{< /details >}}
- **Căn chỉnh in hộp**
  * *Số bản nhân thời gian setup mỗi bản.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTSETUP
  * *Kí hiệu*: {{< katex >}}T_s{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_p * T_s}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_p{{< /katex >}}: Số bản in hộp (Bản)<br>
{{< katex >}}T_s{{< /katex >}}: Thời gian căn chỉnh mỗi bản hộp (Phút/Bản)<br>

  {{< /details >}}
- **Tổng thời gian in**
  * *Chạy máy cộng căn chỉnh bản.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRINTTOTAL
  * *Kí hiệu*: {{< katex >}}T_{print}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_{run} + T_s{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_{run}{{< /katex >}}: Chạy in hộp (Phút)<br>
{{< katex >}}T_s{{< /katex >}}: Căn chỉnh in hộp (Phút)<br>

  {{< /details >}}
- **Bế, cấn và tách phế hộp**
  * *Chạy số tờ tốt qua máy bế/cấn có bộ phận tách phế, cộng setup khuôn và register.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTDIECUT
  * *Kí hiệu*: {{< katex >}}T_d{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_g * 60 / v_d + t_d}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_g{{< /katex >}}: Số tờ tốt cần có (Tờ)<br>
{{< katex >}}v_d{{< /katex >}}: Tốc độ planning máy bế hộp (Tờ/Giờ)<br>
{{< katex >}}t_d{{< /katex >}}: Thời gian chuẩn bị máy bế hộp (Phút)<br>

  {{< /details >}}
- **Gấp và dán hộp**
  * *Gấp đường cấn, bôi keo tai dán và ép đường dán trên folder-gluer.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTGLUE
  * *Kí hiệu*: {{< katex >}}T_g{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q_g * 60 / v_g + t_g}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số hộp mục tiêu trước hao hụt thành phẩm (Hộp)<br>
{{< katex >}}v_g{{< /katex >}}: Tốc độ planning máy gấp dán hộp (Hộp/Giờ)<br>
{{< katex >}}t_g{{< /katex >}}: Thời gian chuẩn bị máy gấp dán hộp (Phút)<br>

  {{< /details >}}
- **Đóng gói hộp phẳng**
  * *Bó hoặc đóng gói đủ sản lượng giao sau gấp dán.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPACK
  * *Kí hiệu*: {{< katex >}}T_b{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{Q / N_b}\rceil * t_b / n_b}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng hộp cần giao (Hộp)<br>
{{< katex >}}N_b{{< /katex >}}: Số hộp mỗi gói (Hộp)<br>
{{< katex >}}t_b{{< /katex >}}: Thời gian đóng một gói hộp (Phút/Gói)<br>
{{< katex >}}n_b{{< /katex >}}: Nhân công đóng gói hộp (Người)<br>

  {{< /details >}}
- **Thời gian hoàn thiện khác**
  * *Ô nhập tay cho khâu hoàn thiện chưa mô hình hoá. Không suy diễn, chỉ lấy đúng số người dùng nhập.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTOTHR
  * *Kí hiệu*: {{< katex >}}T_{other}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_{other}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_{other}{{< /katex >}}: Thời gian hoàn thiện khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian hoàn thiện**
  * *Pha cắt tờ, bế/cấn/tách phế, gấp-dán, đóng gói hộp phẳng và ô hoàn thiện khác.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTFINISH
  * *Kí hiệu*: {{< katex >}}T_{finish}{{< /katex >}}
  * *Công thức* :{{< katex >}}T_c + T_d + T_g + T_b + T_{other}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_c{{< /katex >}}: Pha cắt tờ hộp (Phút)<br>
{{< katex >}}T_d{{< /katex >}}: Bế, cấn và tách phế hộp (Phút)<br>
{{< katex >}}T_g{{< /katex >}}: Gấp và dán hộp (Phút)<br>
{{< katex >}}T_b{{< /katex >}}: Đóng gói hộp phẳng (Phút)<br>
{{< katex >}}T_{other}{{< /katex >}}: Thời gian hoàn thiện khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian sản xuất**
  * *Tổng thời gian chế bản, in offset và hoàn thiện hộp phẳng trong model.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTTOTAL
  * *Kí hiệu*: {{< katex >}}T{{< /katex >}}
  * *Công thức* :{{< katex >}}T_{pre} + T_{print} + T_{finish}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}T_{pre}{{< /katex >}}: Tổng thời gian chế bản (Phút)<br>
{{< katex >}}T_{print}{{< /katex >}}: Tổng thời gian in (Phút)<br>
{{< katex >}}T_{finish}{{< /katex >}}: Tổng thời gian hoàn thiện (Phút)<br>

  {{< /details >}}



