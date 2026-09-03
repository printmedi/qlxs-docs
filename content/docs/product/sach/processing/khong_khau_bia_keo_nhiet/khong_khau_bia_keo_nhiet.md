---
weight: 1
type: docs
title: Công Thức
url: /sach/khong_khau_bia_keo_nhiet
---

# Không khâu bìa keo nhiệt

Sách bìa mềm không khâu (perfect binding): ruột offset tờ rời được gấp, bắt tay,
phay/xử lý gáy, bôi keo gáy, bôi keo hông, vào bìa và xén ba mặt.
Hai profile EVA/PUR dùng chung phần giấy, bản, mực và dây chuyền; chỉ override
tham số phụ thuộc hệ keo. Công thức offset, hình học và khối lượng keo đã được
đối chiếu nguồn hãng và test số. Recipe, hao hụt, tốc độ và giá vẫn phải hiệu
chuẩn theo TDS/SOP cùng dữ liệu thực tế của nhà máy.


# Thông Tin Tính Toán

## Tính Toán
### Tính Toán Nguyên Vật Liệu
- **Số trang ruột sản xuất**
  * *Số trang ruột sau khi bù đủ tay sách.*
  * *Đơn vị*: Trang
  * *Mã*: MATPRODPG
  * *Kí hiệu*: {{< katex >}}p_{prod}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{p_t / i_t}\rceil * i_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_t{{< /katex >}}: Số trang ruột khách hàng (Trang)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>

  {{< /details >}}
- **Tổng số trang khách hàng**
  * *Tổng số trang bìa và ruột khách hàng.*
  * *Đơn vị*: Trang
  * *Mã*: MATSNP
  * *Kí hiệu*: {{< katex >}}p{{< /katex >}}
  * *Công thức* :{{< katex >}}p_c + p_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_c{{< /katex >}}: Số trang bìa (Trang)<br>
{{< katex >}}p_t{{< /katex >}}: Số trang ruột khách hàng (Trang)<br>

  {{< /details >}}
- **Số trang trắng bù tay**
  * *Chênh lệch giữa số trang sản xuất và số trang khách hàng.*
  * *Đơn vị*: Trang
  * *Mã*: MATBLANK
  * *Kí hiệu*: {{< katex >}}p_{blank}{{< /katex >}}
  * *Công thức* :{{< katex >}}p_{prod} - p_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_{prod}{{< /katex >}}: Số trang ruột sản xuất (Trang)<br>
{{< katex >}}p_t{{< /katex >}}: Số trang ruột khách hàng (Trang)<br>

  {{< /details >}}
- **Số khối ruột cần sản xuất**
  * *Sản lượng gộp đã bù hao hụt thành phẩm.*
  * *Đơn vị*: Cuốn
  * *Mã*: MATGROSS
  * *Kí hiệu*: {{< katex >}}Q_g{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q / (1 - w_f)}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng thành phẩm (Cuốn)<br>
{{< katex >}}w_f{{< /katex >}}: Tỷ lệ hao hụt thành phẩm (Tỷ lệ)<br>

  {{< /details >}}
- **Số tay sách mỗi cuốn**
  * *Số tay nguyên vẹn sau bù trang trắng.*
  * *Đơn vị*: Tay/Cuốn
  * *Mã*: MATSIG
  * *Kí hiệu*: {{< katex >}}n_s{{< /katex >}}
  * *Công thức* :{{< katex >}}p_{prod} / i_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_{prod}{{< /katex >}}: Số trang ruột sản xuất (Trang)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>

  {{< /details >}}
- **Số khuôn bìa**
  * *Số khuôn bình bìa cần chạy.*
  * *Đơn vị*: Khuôn
  * *Mã*: MATCOVFORM
  * *Kí hiệu*: {{< katex >}}F_c{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{p_c / i_c}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_c{{< /katex >}}: Số trang bìa (Trang)<br>
{{< katex >}}i_c{{< /katex >}}: Kiểu bình bìa (Trang/tờ)<br>

  {{< /details >}}
- **Số khuôn ruột**
  * *Mỗi tay sách cần một khuôn bình riêng.*
  * *Đơn vị*: Khuôn
  * *Mã*: MATINFORM
  * *Kí hiệu*: {{< katex >}}F_t{{< /katex >}}
  * *Công thức* :{{< katex >}}n_s{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}n_s{{< /katex >}}: Số tay sách mỗi cuốn (Tay/Cuốn)<br>

  {{< /details >}}
- **Số lượt màu bìa**
  * *Số lần chạy để đủ màu theo số đơn vị in của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATCOVCP
  * *Kí hiệu*: {{< katex >}}r_{c,color}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{c_c / \mathcal{M}\mathscr{i}PrterCov_{unit}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}c_c{{< /katex >}}: Số màu in bìa (Màu)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCov_{unit}{{< /katex >}}: Số màu máy in bìa hỗ trợ (Màu)<br>

  {{< /details >}}
- **Số lượt màu ruột**
  * *Số lần chạy để đủ màu theo số đơn vị in của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATINCP
  * *Kí hiệu*: {{< katex >}}r_{t,color}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{c_t / \mathcal{M}\mathscr{i}PrterCon_{unit}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}c_t{{< /katex >}}: Số màu in ruột (Màu)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCon_{unit}{{< /katex >}}: Số màu máy in ruột hỗ trợ (Màu)<br>

  {{< /details >}}
- **Số lượt mặt bìa**
  * *Số lần chạy để đủ mặt theo khả năng trở mặt của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATCOVSP
  * *Kí hiệu*: {{< katex >}}r_{c,side}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{d_c / \mathcal{M}\mathscr{i}PrterCov_{side}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}d_c{{< /katex >}}: Số mặt in bìa (Mặt)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCov_{side}{{< /katex >}}: Số mặt máy in bìa hỗ trợ (Mặt)<br>

  {{< /details >}}
- **Số lượt mặt ruột**
  * *Số lần chạy để đủ mặt theo khả năng trở mặt của máy.*
  * *Đơn vị*: Lượt
  * *Mã*: MATINSP
  * *Kí hiệu*: {{< katex >}}r_{t,side}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{d_t / \mathcal{M}\mathscr{i}PrterCon_{side}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}d_t{{< /katex >}}: Số mặt in ruột (Mặt)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCon_{side}{{< /katex >}}: Số mặt máy in ruột hỗ trợ (Mặt)<br>

  {{< /details >}}
- **Tổng lượt chạy bìa mỗi khuôn**
  * *Tích lượt màu và lượt mặt.*
  * *Đơn vị*: Lượt/Khuôn
  * *Mã*: MATCOVPASS
  * *Kí hiệu*: {{< katex >}}r_c{{< /katex >}}
  * *Công thức* :{{< katex >}}r_{c,color} * r_{c,side}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}r_{c,color}{{< /katex >}}: Số lượt màu bìa (Lượt)<br>
{{< katex >}}r_{c,side}{{< /katex >}}: Số lượt mặt bìa (Lượt)<br>

  {{< /details >}}
- **Tổng lượt chạy ruột mỗi khuôn**
  * *Tích lượt màu và lượt mặt.*
  * *Đơn vị*: Lượt/Khuôn
  * *Mã*: MATINPASS
  * *Kí hiệu*: {{< katex >}}r_t{{< /katex >}}
  * *Công thức* :{{< katex >}}r_{t,color} * r_{t,side}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}r_{t,color}{{< /katex >}}: Số lượt màu ruột (Lượt)<br>
{{< katex >}}r_{t,side}{{< /katex >}}: Số lượt mặt ruột (Lượt)<br>

  {{< /details >}}
- **Tờ bìa tốt tối thiểu**
  * *Tờ tốt cần thiết cho sản lượng gộp.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVNET
  * *Kí hiệu*: {{< katex >}}N_{c,net}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q_g * p_c / i_c}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}p_c{{< /katex >}}: Số trang bìa (Trang)<br>
{{< katex >}}i_c{{< /katex >}}: Kiểu bình bìa (Trang/tờ)<br>

  {{< /details >}}
- **Tờ ruột tốt tối thiểu**
  * *Một tờ cho mỗi tay của mỗi khối ruột.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINNET
  * *Kí hiệu*: {{< katex >}}N_{t,net}{{< /katex >}}
  * *Công thức* :{{< katex >}}Q_g * n_s{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}n_s{{< /katex >}}: Số tay sách mỗi cuốn (Tay/Cuốn)<br>

  {{< /details >}}
- **Tờ chạy bìa sau hao hụt biến đổi**
  * *Tờ chạy sản lượng, chưa gồm make-ready.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVRUN
  * *Kí hiệu*: {{< katex >}}N_{c,run}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_{c,net} / (1 - w_{p,c})}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{c,net}{{< /katex >}}: Tờ bìa tốt tối thiểu (Tờ)<br>
{{< katex >}}w_{p,c}{{< /katex >}}: Tỷ lệ hao hụt chạy bìa (Tỷ lệ)<br>

  {{< /details >}}
- **Tờ chạy ruột sau hao hụt biến đổi**
  * *Tờ chạy sản lượng, chưa gồm make-ready.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINRUN
  * *Kí hiệu*: {{< katex >}}N_{t,run}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{N_{t,net} / (1 - w_{p,t})}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{t,net}{{< /katex >}}: Tờ ruột tốt tối thiểu (Tờ)<br>
{{< katex >}}w_{p,t}{{< /katex >}}: Tỷ lệ hao hụt chạy ruột (Tỷ lệ)<br>

  {{< /details >}}
- **Tờ căn chỉnh bìa**
  * *Make-ready cố định theo khuôn và lượt.*
  * *Đơn vị*: Tờ
  * *Mã*: MATCOVSET
  * *Kí hiệu*: {{< katex >}}N_{c,set}{{< /katex >}}
  * *Công thức* :{{< katex >}}m_c * F_c * r_c{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}m_c{{< /katex >}}: Tờ căn chỉnh bìa mỗi khuôn-lượt (Tờ)<br>
{{< katex >}}F_c{{< /katex >}}: Số khuôn bìa (Khuôn)<br>
{{< katex >}}r_c{{< /katex >}}: Tổng lượt chạy bìa mỗi khuôn (Lượt/Khuôn)<br>

  {{< /details >}}
- **Tờ căn chỉnh ruột**
  * *Make-ready cố định theo khuôn và lượt.*
  * *Đơn vị*: Tờ
  * *Mã*: MATINSET
  * *Kí hiệu*: {{< katex >}}N_{t,set}{{< /katex >}}
  * *Công thức* :{{< katex >}}m_t * F_t * r_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}m_t{{< /katex >}}: Tờ căn chỉnh ruột mỗi khuôn-lượt (Tờ)<br>
{{< katex >}}F_t{{< /katex >}}: Số khuôn ruột (Khuôn)<br>
{{< katex >}}r_t{{< /katex >}}: Tổng lượt chạy ruột mỗi khuôn (Lượt/Khuôn)<br>

  {{< /details >}}
- **Tổng tờ giấy bìa tiêu thụ**
  * *Tờ chạy cộng tờ căn chỉnh.*
  * *Đơn vị*: Tờ
  * *Mã*: MATPNB
  * *Kí hiệu*: {{< katex >}}N_c{{< /katex >}}
  * *Công thức* :{{< katex >}}N_{c,run} + N_{c,set}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{c,run}{{< /katex >}}: Tờ chạy bìa sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}N_{c,set}{{< /katex >}}: Tờ căn chỉnh bìa (Tờ)<br>

  {{< /details >}}
- **Tổng tờ giấy ruột tiêu thụ**
  * *Tờ chạy cộng tờ căn chỉnh.*
  * *Đơn vị*: Tờ
  * *Mã*: MATPNR
  * *Kí hiệu*: {{< katex >}}N_t{{< /katex >}}
  * *Công thức* :{{< katex >}}N_{t,run} + N_{t,set}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{t,run}{{< /katex >}}: Tờ chạy ruột sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}N_{t,set}{{< /katex >}}: Tờ căn chỉnh ruột (Tờ)<br>

  {{< /details >}}
- **Số bản offset bìa**
  * *Một bản cho mỗi khuôn, màu và mặt.*
  * *Đơn vị*: Bản
  * *Mã*: MATPCB
  * *Kí hiệu*: {{< katex >}}P_c{{< /katex >}}
  * *Công thức* :{{< katex >}}F_c * c_c * d_c{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}F_c{{< /katex >}}: Số khuôn bìa (Khuôn)<br>
{{< katex >}}c_c{{< /katex >}}: Số màu in bìa (Màu)<br>
{{< katex >}}d_c{{< /katex >}}: Số mặt in bìa (Mặt)<br>

  {{< /details >}}
- **Số bản offset ruột**
  * *Một bản cho mỗi khuôn, màu và mặt.*
  * *Đơn vị*: Bản
  * *Mã*: MATPCR
  * *Kí hiệu*: {{< katex >}}P_t{{< /katex >}}
  * *Công thức* :{{< katex >}}F_t * c_t * d_t{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}F_t{{< /katex >}}: Số khuôn ruột (Khuôn)<br>
{{< katex >}}c_t{{< /katex >}}: Số màu in ruột (Màu)<br>
{{< katex >}}d_t{{< /katex >}}: Số mặt in ruột (Mặt)<br>

  {{< /details >}}
- **Độ dày khối ruột tại gáy**
  * *Số lá nhân caliper đo được và hệ số hiệu chỉnh sau khâu/nén.*
  * *Đơn vị*: cm
  * *Mã*: MATGS
  * *Kí hiệu*: {{< katex >}}s{{< /katex >}}
  * *Công thức* :{{< katex >}}p_{prod} / 2 * t_t * 0.0001 * k_s{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_{prod}{{< /katex >}}: Số trang ruột sản xuất (Trang)<br>
{{< katex >}}t_t{{< /katex >}}: Caliper giấy ruột (µm)<br>
{{< katex >}}k_s{{< /katex >}}: Hệ số hiệu chỉnh gáy sau khâu và ép (Hệ số)<br>

  {{< /details >}}
- **Khổ bình bìa yêu cầu - dài**
  * *Kích thước bố trí bảo thủ gồm bleed, nhíp và thang màu.*
  * *Đơn vị*: cm
  * *Mã*: MATKIBD
  * *Kí hiệu*: {{< katex >}}L_c{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}i_c{{< /katex >}} bằng [•  4  	]: {{< katex >}}\lceil{((2 * w + s + 2 * b) + g + c) * 10}\rceil / 10{{< /katex >}}
	* Ngoài ra: {{< katex >}}\lceil{(2 * (2 * w + s + 2 * b) + g + c) * 10}\rceil / 10{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}w{{< /katex >}}: Chiều rộng thành phẩm (cm)<br>
{{< katex >}}s{{< /katex >}}: Độ dày khối ruột tại gáy (cm)<br>
{{< katex >}}b{{< /katex >}}: Bleed mỗi cạnh (cm)<br>
{{< katex >}}g{{< /katex >}}: Khoảng chừa nhíp (cm)<br>
{{< katex >}}c{{< /katex >}}: Khoảng thang màu (cm)<br>
{{< katex >}}i_c{{< /katex >}}: Kiểu bình bìa (Trang/tờ)<br>

  {{< /details >}}
- **Khổ bình bìa yêu cầu - rộng**
  * *Kích thước bố trí bảo thủ theo số bìa trên tờ.*
  * *Đơn vị*: cm
  * *Mã*: MATKIBR
  * *Kí hiệu*: {{< katex >}}W_c{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}i_c{{< /katex >}} thuộc [•  4  	•  8  	]: {{< katex >}}\lceil{(h + 2 * b) * 10}\rceil / 10{{< /katex >}}
	* Nếu {{< katex >}}i_c{{< /katex >}} bằng [•  16  	]: {{< katex >}}\lceil{(2 * (h + 2 * b)) * 10}\rceil / 10{{< /katex >}}
	* Ngoài ra: {{< katex >}}\lceil{(4 * (h + 2 * b)) * 10}\rceil / 10{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}h{{< /katex >}}: Chiều dài thành phẩm (cm)<br>
{{< katex >}}b{{< /katex >}}: Bleed mỗi cạnh (cm)<br>
{{< katex >}}i_c{{< /katex >}}: Kiểu bình bìa (Trang/tờ)<br>

  {{< /details >}}
- **Khổ bình ruột yêu cầu - dài**
  * *Grid trang trên một mặt tờ, có bleed, nhíp và thang màu.*
  * *Đơn vị*: cm
  * *Mã*: MATKIRD
  * *Kí hiệu*: {{< katex >}}L_t{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}i_t{{< /katex >}} bằng [•  8  	]: {{< katex >}}\lceil{(2 * (w + d_{mill} + 2 * b) + g + c) * 10}\rceil / 10{{< /katex >}}
	* Ngoài ra: {{< katex >}}\lceil{(4 * (w + d_{mill} + 2 * b) + g + c) * 10}\rceil / 10{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}w{{< /katex >}}: Chiều rộng thành phẩm (cm)<br>
{{< katex >}}d_{mill}{{< /katex >}}: Chiều sâu phay gáy (cm)<br>
{{< katex >}}b{{< /katex >}}: Bleed mỗi cạnh (cm)<br>
{{< katex >}}g{{< /katex >}}: Khoảng chừa nhíp (cm)<br>
{{< katex >}}c{{< /katex >}}: Khoảng thang màu (cm)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>

  {{< /details >}}
- **Khổ bình ruột yêu cầu - rộng**
  * *Grid trang trên một mặt tờ theo kiểu bình.*
  * *Đơn vị*: cm
  * *Mã*: MATKIRR
  * *Kí hiệu*: {{< katex >}}W_t{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}i_t{{< /katex >}} thuộc [•  8  	•  16  	]: {{< katex >}}\lceil{(2 * (h + 2 * b)) * 10}\rceil / 10{{< /katex >}}
	* Ngoài ra: {{< katex >}}\lceil{(4 * (h + 2 * b)) * 10}\rceil / 10{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}h{{< /katex >}}: Chiều dài thành phẩm (cm)<br>
{{< katex >}}b{{< /katex >}}: Bleed mỗi cạnh (cm)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>

  {{< /details >}}
- **Bìa vừa tờ chạy**
  * *1 nếu khổ bình vừa tờ chạy ở ít nhất một hướng xoay.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDC
  * *Kí hiệu*: {{< katex >}}V_c{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}L_c{{< /katex >}} thỏa mãn {{< katex >}}((L_c <= S_{c,l} && W_c <= S_{c,w}) || (L_c <= S_{c,w} && W_c <= S_{c,l})){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_c{{< /katex >}}: Khổ bình bìa yêu cầu - dài (cm)<br>
{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}W_c{{< /katex >}}: Khổ bình bìa yêu cầu - rộng (cm)<br>
{{< katex >}}S_{c,w}{{< /katex >}}: Khổ tờ chạy bìa - rộng (cm)<br>

  {{< /details >}}
- **Ruột vừa tờ chạy**
  * *1 nếu khổ bình vừa tờ chạy ở ít nhất một hướng xoay.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDT
  * *Kí hiệu*: {{< katex >}}V_t{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}L_t{{< /katex >}} thỏa mãn {{< katex >}}((L_t <= S_{t,l} && W_t <= S_{t,w}) || (L_t <= S_{t,w} && W_t <= S_{t,l})){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}L_t{{< /katex >}}: Khổ bình ruột yêu cầu - dài (cm)<br>
{{< katex >}}S_{t,l}{{< /katex >}}: Khổ tờ chạy ruột - dài (cm)<br>
{{< katex >}}W_t{{< /katex >}}: Khổ bình ruột yêu cầu - rộng (cm)<br>
{{< katex >}}S_{t,w}{{< /katex >}}: Khổ tờ chạy ruột - rộng (cm)<br>

  {{< /details >}}
- **Tờ bìa vừa máy**
  * *1 nếu tờ chạy bìa vừa khổ máy ở ít nhất một hướng.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDMC
  * *Kí hiệu*: {{< katex >}}V_{mc}{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}S_{c,l}{{< /katex >}} thỏa mãn {{< katex >}}((S_{c,l} <= M_{c,l} && S_{c,w} <= M_{c,w}) || (S_{c,l} <= M_{c,w} && S_{c,w} <= M_{c,l})){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}M_{c,l}{{< /katex >}}: Khổ máy in bìa - dài (cm)<br>
{{< katex >}}S_{c,w}{{< /katex >}}: Khổ tờ chạy bìa - rộng (cm)<br>
{{< katex >}}M_{c,w}{{< /katex >}}: Khổ máy in bìa - rộng (cm)<br>

  {{< /details >}}
- **Tờ ruột vừa máy**
  * *1 nếu tờ chạy ruột vừa khổ máy ở ít nhất một hướng.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDMT
  * *Kí hiệu*: {{< katex >}}V_{mt}{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}S_{t,l}{{< /katex >}} thỏa mãn {{< katex >}}((S_{t,l} <= M_{t,l} && S_{t,w} <= M_{t,w}) || (S_{t,l} <= M_{t,w} && S_{t,w} <= M_{t,l})){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}S_{t,l}{{< /katex >}}: Khổ tờ chạy ruột - dài (cm)<br>
{{< katex >}}M_{t,l}{{< /katex >}}: Khổ máy in ruột - dài (cm)<br>
{{< katex >}}S_{t,w}{{< /katex >}}: Khổ tờ chạy ruột - rộng (cm)<br>
{{< katex >}}M_{t,w}{{< /katex >}}: Khổ máy in ruột - rộng (cm)<br>

  {{< /details >}}
- **Gáy trong giới hạn máy đóng cuốn**
  * *1 nếu độ dày gáy nằm trong giới hạn cấu hình.*
  * *Đơn vị*: Boolean
  * *Mã*: MATVALIDS
  * *Kí hiệu*: {{< katex >}}V_s{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}s{{< /katex >}} thỏa mãn {{< katex >}}(s * 10 >= s_{min} && s * 10 <= s_{max}){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}s{{< /katex >}}: Độ dày khối ruột tại gáy (cm)<br>
{{< katex >}}s_{min}{{< /katex >}}: Độ dày đóng cuốn tối thiểu (mm)<br>
{{< katex >}}s_{max}{{< /katex >}}: Độ dày đóng cuốn tối đa (mm)<br>

  {{< /details >}}
- **Khối lượng giấy bìa**
  * *Tổng tờ vật lý nhân diện tích tờ chạy và định lượng.*
  * *Đơn vị*: Tấn
  * *Mã*: MATPWB
  * *Kí hiệu*: {{< katex >}}W_c{{< /katex >}}
  * *Công thức* :{{< katex >}}N_c * S_{c,l} * S_{c,w} * gsm_c * 0.0000000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_c{{< /katex >}}: Tổng tờ giấy bìa tiêu thụ (Tờ)<br>
{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}S_{c,w}{{< /katex >}}: Khổ tờ chạy bìa - rộng (cm)<br>
{{< katex >}}gsm_c{{< /katex >}}: Định lượng giấy bìa (g/m²)<br>

  {{< /details >}}
- **Khối lượng giấy ruột**
  * *Tổng tờ vật lý nhân diện tích tờ chạy và định lượng.*
  * *Đơn vị*: Tấn
  * *Mã*: MATPWR
  * *Kí hiệu*: {{< katex >}}W_t{{< /katex >}}
  * *Công thức* :{{< katex >}}N_t * S_{t,l} * S_{t,w} * gsm_t * 0.0000000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng tờ giấy ruột tiêu thụ (Tờ)<br>
{{< katex >}}S_{t,l}{{< /katex >}}: Khổ tờ chạy ruột - dài (cm)<br>
{{< katex >}}S_{t,w}{{< /katex >}}: Khổ tờ chạy ruột - rộng (cm)<br>
{{< katex >}}gsm_t{{< /katex >}}: Định lượng giấy ruột (g/m²)<br>

  {{< /details >}}
- **Khối lượng mực bìa**
  * *Tờ-màu-mặt nhân diện tích, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: MATIWB
  * *Kí hiệu*: {{< katex >}}I_c{{< /katex >}}
  * *Công thức* :{{< katex >}}((N_{c,run} * c_c * d_c) + (N_{c,set} * (c_c / r_{c,color}) * (d_c / r_{c,side}))) * S_{c,l} * S_{c,w} * a_c * f_{ink} * 0.000000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{c,run}{{< /katex >}}: Tờ chạy bìa sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}c_c{{< /katex >}}: Số màu in bìa (Màu)<br>
{{< katex >}}d_c{{< /katex >}}: Số mặt in bìa (Mặt)<br>
{{< katex >}}N_{c,set}{{< /katex >}}: Tờ căn chỉnh bìa (Tờ)<br>
{{< katex >}}r_{c,color}{{< /katex >}}: Số lượt màu bìa (Lượt)<br>
{{< katex >}}r_{c,side}{{< /katex >}}: Số lượt mặt bìa (Lượt)<br>
{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}S_{c,w}{{< /katex >}}: Khổ tờ chạy bìa - rộng (cm)<br>
{{< katex >}}a_c{{< /katex >}}: Độ phủ trung bình mỗi màu bìa (%)<br>
{{< katex >}}f_{ink}{{< /katex >}}: Định mức màng mực tại 100% phủ (g/m²)<br>

  {{< /details >}}
- **Khối lượng mực ruột**
  * *Tờ-màu-mặt nhân diện tích, độ phủ và định mức màng mực.*
  * *Đơn vị*: kg
  * *Mã*: MATIWR
  * *Kí hiệu*: {{< katex >}}I_t{{< /katex >}}
  * *Công thức* :{{< katex >}}((N_{t,run} * c_t * d_t) + (N_{t,set} * (c_t / r_{t,color}) * (d_t / r_{t,side}))) * S_{t,l} * S_{t,w} * a_t * f_{ink} * 0.000000001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{t,run}{{< /katex >}}: Tờ chạy ruột sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}c_t{{< /katex >}}: Số màu in ruột (Màu)<br>
{{< katex >}}d_t{{< /katex >}}: Số mặt in ruột (Mặt)<br>
{{< katex >}}N_{t,set}{{< /katex >}}: Tờ căn chỉnh ruột (Tờ)<br>
{{< katex >}}r_{t,color}{{< /katex >}}: Số lượt màu ruột (Lượt)<br>
{{< katex >}}r_{t,side}{{< /katex >}}: Số lượt mặt ruột (Lượt)<br>
{{< katex >}}S_{t,l}{{< /katex >}}: Khổ tờ chạy ruột - dài (cm)<br>
{{< katex >}}S_{t,w}{{< /katex >}}: Khổ tờ chạy ruột - rộng (cm)<br>
{{< katex >}}a_t{{< /katex >}}: Độ phủ trung bình mỗi màu ruột (%)<br>
{{< katex >}}f_{ink}{{< /katex >}}: Định mức màng mực tại 100% phủ (g/m²)<br>

  {{< /details >}}
- **Diện tích màng bìa**
  * *Diện tích tờ bìa tiêu thụ nhân số mặt cán.*
  * *Đơn vị*: m²
  * *Mã*: MATFILM
  * *Kí hiệu*: {{< katex >}}A_f{{< /katex >}}
  * *Công thức* :{{< katex >}}N_c * S_{c,l} * S_{c,w} * n_{lam} * 0.0001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_c{{< /katex >}}: Tổng tờ giấy bìa tiêu thụ (Tờ)<br>
{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}S_{c,w}{{< /katex >}}: Khổ tờ chạy bìa - rộng (cm)<br>
{{< katex >}}n_{lam}{{< /katex >}}: Số mặt cán màng bìa (Mặt)<br>

  {{< /details >}}
- **Chiều dài màng chạy**
  * *Tổng chiều dài tờ bìa qua máy cán, nhân số mặt cán.*
  * *Đơn vị*: m
  * *Mã*: MATFILMLEN
  * *Kí hiệu*: {{< katex >}}l_f{{< /katex >}}
  * *Công thức* :{{< katex >}}N_c * S_{c,l} * n_{lam} * 0.01{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_c{{< /katex >}}: Tổng tờ giấy bìa tiêu thụ (Tờ)<br>
{{< katex >}}S_{c,l}{{< /katex >}}: Khổ tờ chạy bìa - dài (cm)<br>
{{< katex >}}n_{lam}{{< /katex >}}: Số mặt cán màng bìa (Mặt)<br>

  {{< /details >}}
- **Chi phí giấy**
  * *Chi phí giấy bìa và ruột theo khối lượng riêng.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCG
  * *Kí hiệu*: {{< katex >}}C_p{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{W_c * P_{paper,cover} + W_t * P_{paper,text}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}W_c{{< /katex >}}: Khối lượng giấy bìa (Tấn)<br>
{{< katex >}}P_{paper,cover}{{< /katex >}}: Đơn giá giấy bìa (VNĐ/Tấn)<br>
{{< katex >}}W_t{{< /katex >}}: Khối lượng giấy ruột (Tấn)<br>
{{< katex >}}P_{paper,text}{{< /katex >}}: Đơn giá giấy ruột (VNĐ/Tấn)<br>

  {{< /details >}}
- **Chi phí vật tư bản**
  * *Số bản nhân đúng diện tích bản tương ứng.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCBI
  * *Kí hiệu*: {{< katex >}}C_{plate}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(P_c * B_{c,l} * B_{c,w} + P_t * B_{t,l} * B_{t,w}) * P_{plate}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}P_c{{< /katex >}}: Số bản offset bìa (Bản)<br>
{{< katex >}}B_{c,l}{{< /katex >}}: Khổ bản bìa - dài (cm)<br>
{{< katex >}}B_{c,w}{{< /katex >}}: Khổ bản bìa - rộng (cm)<br>
{{< katex >}}P_t{{< /katex >}}: Số bản offset ruột (Bản)<br>
{{< katex >}}B_{t,l}{{< /katex >}}: Khổ bản ruột - dài (cm)<br>
{{< katex >}}B_{t,w}{{< /katex >}}: Khổ bản ruột - rộng (cm)<br>
{{< katex >}}P_{plate}{{< /katex >}}: Đơn giá bản offset (VNĐ/cm²)<br>

  {{< /details >}}
- **Chi phí mực**
  * *Khối lượng mực nhân đơn giá; không nhân lại số bản.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCMI
  * *Kí hiệu*: {{< katex >}}C_{ink}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(I_c + I_t) * P_{ink}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}I_c{{< /katex >}}: Khối lượng mực bìa (kg)<br>
{{< katex >}}I_t{{< /katex >}}: Khối lượng mực ruột (kg)<br>
{{< katex >}}P_{ink}{{< /katex >}}: Đơn giá mực (VNĐ/kg)<br>

  {{< /details >}}
- **Chi phí màng**
  * *Diện tích màng theo m² nhân đơn giá.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCMB
  * *Kí hiệu*: {{< katex >}}C_f{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{A_f * P_{film}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_f{{< /katex >}}: Diện tích màng bìa (m²)<br>
{{< katex >}}P_{film}{{< /katex >}}: Đơn giá màng bìa (VNĐ/m²)<br>

  {{< /details >}}
- **Chi phí chế bản**
  * *Chi phí dịch vụ trên tổng số bản offset.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCCB
  * *Kí hiệu*: {{< katex >}}C_{prep}{{< /katex >}}
  * *Công thức* :{{< katex >}}(P_c + P_t) * C_{prepress}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}P_c{{< /katex >}}: Số bản offset bìa (Bản)<br>
{{< katex >}}P_t{{< /katex >}}: Số bản offset ruột (Bản)<br>
{{< katex >}}C_{prepress}{{< /katex >}}: Chi phí chế bản mỗi bản (VNĐ/Bản)<br>

  {{< /details >}}
- **Chi phí chạy máy in**
  * *Setup theo khuôn-lượt cộng chi phí biến đổi theo lượt tờ.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCPR
  * *Kí hiệu*: {{< katex >}}C_{press}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(F_c * r_c + F_t * r_t) * C_{setup} + (N_{c,run} * r_c + N_{t,run} * r_t + N_{c,set} + N_{t,set}) * C_{impression}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}F_c{{< /katex >}}: Số khuôn bìa (Khuôn)<br>
{{< katex >}}r_c{{< /katex >}}: Tổng lượt chạy bìa mỗi khuôn (Lượt/Khuôn)<br>
{{< katex >}}F_t{{< /katex >}}: Số khuôn ruột (Khuôn)<br>
{{< katex >}}r_t{{< /katex >}}: Tổng lượt chạy ruột mỗi khuôn (Lượt/Khuôn)<br>
{{< katex >}}C_{setup}{{< /katex >}}: Chi phí setup mỗi khuôn-lượt (VNĐ)<br>
{{< katex >}}N_{c,run}{{< /katex >}}: Tờ chạy bìa sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}N_{t,run}{{< /katex >}}: Tờ chạy ruột sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}N_{c,set}{{< /katex >}}: Tờ căn chỉnh bìa (Tờ)<br>
{{< katex >}}N_{t,set}{{< /katex >}}: Tờ căn chỉnh ruột (Tờ)<br>
{{< katex >}}C_{impression}{{< /katex >}}: Chi phí mỗi lượt tờ qua máy (VNĐ/Lượt tờ)<br>

  {{< /details >}}
- **Chi phí hoàn thiện**
  * *Phần theo tay sách cộng phần theo cuốn trên sản lượng gộp.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCGC
  * *Kí hiệu*: {{< katex >}}C_{finish}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{Q_g * n_s * C_{signature} + Q_g * C_{book} + C_{glue}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}n_s{{< /katex >}}: Số tay sách mỗi cuốn (Tay/Cuốn)<br>
{{< katex >}}C_{signature}{{< /katex >}}: Chi phí hoàn thiện mỗi tay sách (VNĐ/Tay)<br>
{{< katex >}}C_{book}{{< /katex >}}: Chi phí hoàn thiện mỗi cuốn (VNĐ/Cuốn)<br>
{{< katex >}}C_{glue}{{< /katex >}}: Chi phí vật tư keo đóng cuốn (VNĐ)<br>

  {{< /details >}}
- **Chi phí đơn hàng**
  * *Tổng vật tư, chế bản, chạy máy, hoàn thiện và khoản khác.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATPRCDH
  * *Kí hiệu*: {{< katex >}}C_{order}{{< /katex >}}
  * *Công thức* :{{< katex >}}C_p + C_{plate} + C_{ink} + C_f + C_{prep} + C_{press} + C_pC + C_{other}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_p{{< /katex >}}: Chi phí giấy (VNĐ)<br>
{{< katex >}}C_{plate}{{< /katex >}}: Chi phí vật tư bản (VNĐ)<br>
{{< katex >}}C_{ink}{{< /katex >}}: Chi phí mực (VNĐ)<br>
{{< katex >}}C_f{{< /katex >}}: Chi phí màng (VNĐ)<br>
{{< katex >}}C_{prep}{{< /katex >}}: Chi phí chế bản (VNĐ)<br>
{{< katex >}}C_{press}{{< /katex >}}: Chi phí chạy máy in (VNĐ)<br>
{{< katex >}}C_{finish}{{< /katex >}}: Chi phí hoàn thiện (VNĐ)<br>
{{< katex >}}C_{other}{{< /katex >}}: Chi phí đơn hàng khác (VNĐ)<br>

  {{< /details >}}
- **Chi phí tính toán mỗi cuốn giao**
  * *Chi phí đơn hàng chia số cuốn tốt cần giao; chưa phải báo giá bán.*
  * *Đơn vị*: VNĐ/Cuốn
  * *Mã*: MATPRSIN
  * *Kí hiệu*: {{< katex >}}C_u{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{C_{order} / Q}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}C_{order}{{< /katex >}}: Chi phí đơn hàng (VNĐ)<br>
{{< katex >}}Q{{< /katex >}}: Số lượng thành phẩm (Cuốn)<br>

  {{< /details >}}
- **Diện tích gáy phủ keo**
  * *Tổng diện tích mặt gáy của sản lượng gộp, dùng chiều cao thành phẩm và độ dày khối ruột.*
  * *Đơn vị*: m²
  * *Mã*: MATGLUEAREA
  * *Kí hiệu*: {{< katex >}}A_{spine}{{< /katex >}}
  * *Công thức* :{{< katex >}}Q_g * (h + 2 * a_{trim}) * s * 0.0001{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}h{{< /katex >}}: Chiều dài thành phẩm (cm)<br>
{{< katex >}}a_{trim}{{< /katex >}}: Lượng dư xén đầu/chân mỗi đầu (cm)<br>
{{< katex >}}s{{< /katex >}}: Độ dày khối ruột tại gáy (cm)<br>

  {{< /details >}}
- **Khối lượng keo gáy tiêu thụ**
  * *Diện tích gáy nhân độ dày màng và khối lượng riêng, bù hao hụt hệ keo gáy.*
  * *Đơn vị*: kg
  * *Mã*: MATGLUESPKG
  * *Kí hiệu*: {{< katex >}}M_{glue,spine}{{< /katex >}}
  * *Công thức* :{{< katex >}}A_{spine} * t_{glue} * rho_{glue} / (1 - w_{glue,spine}){{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}A_{spine}{{< /katex >}}: Diện tích gáy phủ keo (m²)<br>
{{< katex >}}t_{glue}{{< /katex >}}: Độ dày màng keo gáy (mm)<br>
{{< katex >}}rho_{glue}{{< /katex >}}: Khối lượng riêng keo gáy (g/cm³)<br>
{{< katex >}}w_{glue,spine}{{< /katex >}}: Tỷ lệ hao hụt keo gáy (Hệ số)<br>

  {{< /details >}}
- **Khối lượng keo hông EVA tiêu thụ**
  * *Hai đường keo hông theo chiều cao gáy, bù hao hụt riêng của hệ keo hông.*
  * *Đơn vị*: kg
  * *Mã*: MATGLUESIKG
  * *Kí hiệu*: {{< katex >}}M_{glue,side}{{< /katex >}}
  * *Công thức* :{{< katex >}}Q_g * 2 * (h + 2 * a_{trim}) * m_{side} * 0.00001 / (1 - w_{glue,side}){{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}h{{< /katex >}}: Chiều dài thành phẩm (cm)<br>
{{< katex >}}a_{trim}{{< /katex >}}: Lượng dư xén đầu/chân mỗi đầu (cm)<br>
{{< katex >}}m_{side}{{< /katex >}}: Định mức keo hông EVA theo chiều dài (g/m)<br>
{{< katex >}}w_{glue,side}{{< /katex >}}: Tỷ lệ hao hụt keo hông (Hệ số)<br>

  {{< /details >}}
- **Tổng khối lượng keo đóng cuốn**
  * *Tổng keo gáy theo profile và keo hông EVA.*
  * *Đơn vị*: kg
  * *Mã*: MATGLUETOT
  * *Kí hiệu*: {{< katex >}}M_{glue}{{< /katex >}}
  * *Công thức* :{{< katex >}}M_{glue,spine} + M_{glue,side}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}M_{glue,spine}{{< /katex >}}: Khối lượng keo gáy tiêu thụ (kg)<br>
{{< katex >}}M_{glue,side}{{< /katex >}}: Khối lượng keo hông EVA tiêu thụ (kg)<br>

  {{< /details >}}
- **Chi phí vật tư keo đóng cuốn**
  * *Keo gáy và keo hông nhân đơn giá mua thực tế tương ứng.*
  * *Đơn vị*: VNĐ
  * *Mã*: MATGLUECOST
  * *Kí hiệu*: {{< katex >}}C_{glue}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{M_{glue,spine} * c_{glue,spine} + M_{glue,side} * c_{glue,side}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}M_{glue,spine}{{< /katex >}}: Khối lượng keo gáy tiêu thụ (kg)<br>
{{< katex >}}c_{glue,spine}{{< /katex >}}: Đơn giá keo gáy (VNĐ/kg)<br>
{{< katex >}}M_{glue,side}{{< /katex >}}: Khối lượng keo hông EVA tiêu thụ (kg)<br>
{{< katex >}}c_{glue,side}{{< /katex >}}: Đơn giá keo hông EVA (VNĐ/kg)<br>

  {{< /details >}}
- **Độ dày màng keo trong giới hạn recipe**
  * *1 nếu độ dày màng keo nằm trong giới hạn TDS/recipe máy đã khai báo.*
  * *Đơn vị*: Boolean
  * *Mã*: MATGLUEVALID
  * *Kí hiệu*: {{< katex >}}V_{glue}{{< /katex >}}
  * *Công thức* :
	* Nếu {{< katex >}}t_{glue}{{< /katex >}} thỏa mãn {{< katex >}}(t_{glue} >= t_{glue,min} && t_{glue} <= t_{glue,max}){{< /katex >}}: {{< katex >}}1{{< /katex >}}
	* Ngoài ra: {{< katex >}}0{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}t_{glue}{{< /katex >}}: Độ dày màng keo gáy (mm)<br>
{{< katex >}}t_{glue,min}{{< /katex >}}: Độ dày keo gáy tối thiểu theo recipe (mm)<br>
{{< katex >}}t_{glue,max}{{< /katex >}}: Độ dày keo gáy tối đa theo recipe (mm)<br>

  {{< /details >}}
- **Thời gian chờ QC keo ngoài máy**
  * *Mốc chờ QC/release theo profile; không cộng vào thời gian chiếm dụng máy hoặc tổng thời gian sản xuất.*
  * *Đơn vị*: Giờ
  * *Mã*: MATGLUEQCH
  * *Kí hiệu*: {{< katex >}}T_{qc}{{< /katex >}}
  * *Công thức* :{{< katex >}}t_{qc}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}t_{qc}{{< /katex >}}: Thời gian chờ đạt điều kiện QC keo (Giờ)<br>

  {{< /details >}}
### Tính Toán Thời Gian
- **Soát lỗi, kiểm tra file chữ**
  * *Thời gian soát lỗi, kiểm tra file chữ*
  * *Đơn vị*: Phút
  * *Mã*: CHRKTT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{txt}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{p * (r/(r + 1)) / (\mathcal{C}\mathscr{i}Det_{txt} * \mathcal{C}\mathscr{i}No_{txt})}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p{{< /katex >}}: Tổng số trang khách hàng (Trang)<br>
{{< katex >}}r{{< /katex >}}: Tỷ lệ trang chữ trên trang ảnh (Hệ số)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{txt}{{< /katex >}}: Năng lực soát lỗi, kiểm tra file chữ (Trang/Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}No_{txt}{{< /katex >}}: Nhân lực soát lỗi, kiểm tra file chữ (Người|Thiết bị)<br>

  {{< /details >}}
- **Xử lý ảnh, kiểm tra file ảnh**
  * *Thời gian xử lý ảnh, kiểm tra file ảnh*
  * *Đơn vị*: Phút
  * *Mã*: CHRKTI
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{img}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{p * (1/(r+1)) / (\mathcal{C}\mathscr{i}Det_{img} * \mathcal{C}\mathscr{i}No_{img})}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p{{< /katex >}}: Tổng số trang khách hàng (Trang)<br>
{{< katex >}}r{{< /katex >}}: Tỷ lệ trang chữ trên trang ảnh (Hệ số)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{img}{{< /katex >}}: Năng lực xử lý ảnh, kiểm tra file ảnh (Trang/Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}No_{img}{{< /katex >}}: Nhân lực xử lý ảnh, kiểm tra file ảnh (Người|Thiết bị)<br>

  {{< /details >}}
- **Dàn trang**
  * *Thời gian dàn trang (layout)*
  * *Đơn vị*: Phút
  * *Mã*: CHRTDT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}T_{layout}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{p * \mathcal{C}\mathscr{i}Det_{layout}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p{{< /katex >}}: Tổng số trang khách hàng (Trang)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{layout}{{< /katex >}}: Năng lực xử lý dàn trang (Phút/Trang)<br>

  {{< /details >}}
- **Bình bản**
  * *Thời gian bình bản (Makeready)*
  * *Đơn vị*: Phút
  * *Mã*: CHRTBB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Makeready{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{i}Det_{makeready}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Det_{makeready}{{< /katex >}}: Định mức thời gian bình bản (Phút)<br>

  {{< /details >}}
- **In thử**
  * *Thời gian in thử*
  * *Đơn vị*: Phút
  * *Mã*: CHRTIT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}test_print{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(((p_t/i_t)*d_t + d_c))/\mathcal{C}\mathscr{i}Det_{vtpr} + \mathcal{C}\mathscr{i}Det_{cbtpr}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}p_t{{< /katex >}}: Số trang ruột khách hàng (Trang)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>
{{< katex >}}d_t{{< /katex >}}: Số mặt in ruột (Mặt)<br>
{{< katex >}}d_c{{< /katex >}}: Số mặt in bìa (Mặt)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{vtpr}{{< /katex >}}: Tốc độ in thử (Tờ/Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{cbtpr}{{< /katex >}}: Thời gian chuẩn bị in thử (Phút)<br>

  {{< /details >}}
- **RIP**
  * *Thời gian RIP (Raster Image Processor).*
  * *Đơn vị*: Phút
  * *Mã*: CHRTRIP
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}rip{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{((F_t * d_t + F_c * d_c)) / \mathcal{C}\mathscr{i}Det_{rip}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}F_t{{< /katex >}}: Số khuôn ruột (Khuôn)<br>
{{< katex >}}d_t{{< /katex >}}: Số mặt in ruột (Mặt)<br>
{{< katex >}}F_c{{< /katex >}}: Số khuôn bìa (Khuôn)<br>
{{< katex >}}d_c{{< /katex >}}: Số mặt in bìa (Mặt)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{rip}{{< /katex >}}: Tốc độ RIP (Mặt/Phút)<br>

  {{< /details >}}
- **Ghi hiện bản**
  * *Thời gian ghi hiện bản (Platemaking).*
  * *Đơn vị*: Phút
  * *Mã*: CHRTPLM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}platemaking{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(P_c + P_t) * \mathcal{C}\mathscr{i}Det_{platemaking}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}P_c{{< /katex >}}: Số bản offset bìa (Bản)<br>
{{< katex >}}P_t{{< /katex >}}: Số bản offset ruột (Bản)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{platemaking}{{< /katex >}}: Tốc độ ghi hiện bản (Phút/Bản)<br>

  {{< /details >}}
- **Thời gian chế bản khác**
  * *Thời gian chế bản khác.*
  * *Đơn vị*: Phút
  * *Mã*: CHRDOTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{preprocessing}{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{i}Other_{PreprocessingInput}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Other_{PreprocessingInput}{{< /katex >}}: Thời gian chế bản khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian chế bản**
  * *Toàn bộ thời gian chế bản*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMPP
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}PPR{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{txt} + \mathcal{C}\mathscr{pp}Ktr_{img} + \mathcal{C}\mathscr{pp}T_{layout} + \mathcal{C}\mathscr{pp}Makeready + \mathcal{C}\mathscr{pp}test_print + \mathcal{C}\mathscr{pp}rip + \mathcal{C}\mathscr{pp}platemaking + \mathcal{C}\mathscr{i}Other_{preprocessing}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{txt}{{< /katex >}}: Soát lỗi, kiểm tra file chữ (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{img}{{< /katex >}}: Xử lý ảnh, kiểm tra file ảnh (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}T_{layout}{{< /katex >}}: Dàn trang (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}Makeready{{< /katex >}}: Bình bản (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}test_print{{< /katex >}}: In thử (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}rip{{< /katex >}}: RIP (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pp}platemaking{{< /katex >}}: Ghi hiện bản (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Other_{preprocessing}{{< /katex >}}: Thời gian chế bản khác (Phút)<br>

  {{< /details >}}
- **In bìa**
  * *Thời gian in bìa trong quá trình sản xuất*
  * *Đơn vị*: Phút
  * *Mã*: CHRPRCOV
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}P_{cover}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(N_{c,run} * r_c) * 60 / \mathcal{M}\mathscr{i}PrterCov_{speed}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{c,run}{{< /katex >}}: Tờ chạy bìa sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}r_c{{< /katex >}}: Tổng lượt chạy bìa mỗi khuôn (Lượt/Khuôn)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCov_{speed}{{< /katex >}}: Tốc độ máy in bìa (Tờ/Giờ)<br>

  {{< /details >}}
- **In ruột**
  * *Thời gian in ruột trong quá trình sản xuất*
  * *Đơn vị*: Phút
  * *Mã*: CHRPRCON
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}P_{content}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(N_{t,run} * r_t) * 60 / \mathcal{M}\mathscr{i}PrterCon_{speed}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_{t,run}{{< /katex >}}: Tờ chạy ruột sau hao hụt biến đổi (Tờ)<br>
{{< katex >}}r_t{{< /katex >}}: Tổng lượt chạy ruột mỗi khuôn (Lượt/Khuôn)<br>
{{< katex >}}\mathcal{M}\mathscr{i}PrterCon_{speed}{{< /katex >}}: Tốc độ máy in ruột (Tờ/Giờ)<br>

  {{< /details >}}
- **Căn chỉnh in bìa**
  * *Thời gian make-ready máy in cho bìa (lắp bản, canh mực, canh chồng màu). Tách riêng khỏi thời gian chạy in; = số bản in × phút mỗi bản (số bản = khuôn × màu × mặt).*
  * *Đơn vị*: Phút
  * *Mã*: CHRCCINB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}Mk_{cover}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{P_c * \mathcal{C}\mathscr{i}Prep_{PrintCover}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}P_c{{< /katex >}}: Số bản offset bìa (Bản)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Prep_{PrintCover}{{< /katex >}}: Căn chỉnh in bìa — phút mỗi bản (Phút/Bản)<br>

  {{< /details >}}
- **Căn chỉnh in ruột**
  * *Thời gian make-ready máy in cho ruột (lắp bản, canh mực, canh chồng màu). Tách riêng khỏi thời gian chạy in; = số bản in × phút mỗi bản (số bản = khuôn × màu × mặt).*
  * *Đơn vị*: Phút
  * *Mã*: CHRCCINR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}Mk_{content}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{P_t * \mathcal{C}\mathscr{i}Prep_{PrintContent}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}P_t{{< /katex >}}: Số bản offset ruột (Bản)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Prep_{PrintContent}{{< /katex >}}: Căn chỉnh in ruột — phút mỗi bản (Phút/Bản)<br>

  {{< /details >}}
- **Thời gian in khác**
  * *Thời gian in khác.*
  * *Đơn vị*: Phút
  * *Mã*: CHRPROTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{printing}{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{i}Other_{PrintingInput}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Other_{PrintingInput}{{< /katex >}}: Thời gian in khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian in**
  * *Toàn bộ thời gian in*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMPR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}PRT{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{pr}P_{cover} + \mathcal{C}\mathscr{pr}P_{content} + \mathcal{C}\mathscr{pr}Mk_{cover} + \mathcal{C}\mathscr{pr}Mk_{content} + \mathcal{C}\mathscr{i}Other_{printing}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{pr}P_{cover}{{< /katex >}}: In bìa (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pr}P_{content}{{< /katex >}}: In ruột (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pr}Mk_{cover}{{< /katex >}}: Căn chỉnh in bìa (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{pr}Mk_{content}{{< /katex >}}: Căn chỉnh in ruột (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Other_{printing}{{< /katex >}}: Thời gian in khác (Phút)<br>

  {{< /details >}}
- **Cán màng**
  * *Công thức tính thời gian cán màng*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGCM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Lamination{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\mathcal{C}\mathscr{i}Det_{machinepreparation} + (l_f / \mathcal{C}\mathscr{i}Det_{processing})}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Det_{machinepreparation}{{< /katex >}}: Thời gian chuẩn bị máy cán màng (Phút)<br>
{{< katex >}}l_f{{< /katex >}}: Chiều dài màng chạy (m)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{processing}{{< /katex >}}: Tốc độ cán màng (m/Phút)<br>

  {{< /details >}}
- **Pha cắt bìa**
  * *Công thức tính thời gian pha cắt bìa*
  * *Đơn vị*: Phút
  * *Mã*: CHRKFPB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{cover}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{(N_c * t_c * 0.0001) / \mathcal{C}\mathscr{i}DetPackHeight_{cover}}\rceil * \mathcal{C}\mathscr{i}DetKnifePhase_{cover}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_c{{< /katex >}}: Tổng tờ giấy bìa tiêu thụ (Tờ)<br>
{{< katex >}}t_c{{< /katex >}}: Caliper giấy bìa (µm)<br>
{{< katex >}}\mathcal{C}\mathscr{i}DetPackHeight_{cover}{{< /katex >}}: Chiều cao tối đa của chồng cắt - bìa (CM)<br>
{{< katex >}}\mathcal{C}\mathscr{i}DetKnifePhase_{cover}{{< /katex >}}: Thời gian chuẩn bị và cắt một nhát - bìa (Phút/Chồng)<br>

  {{< /details >}}
- **Pha cắt ruột**
  * *Công thức tính thời gian pha cắt ruột*
  * *Đơn vị*: Phút
  * *Mã*: CHRKFPR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{content}{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{(N_t * t_t * 0.0001) / \mathcal{C}\mathscr{i}DetPackHeight_{content}}\rceil * \mathcal{C}\mathscr{i}DetKnifePhase_{content}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng tờ giấy ruột tiêu thụ (Tờ)<br>
{{< katex >}}t_t{{< /katex >}}: Caliper giấy ruột (µm)<br>
{{< katex >}}\mathcal{C}\mathscr{i}DetPackHeight_{content}{{< /katex >}}: Chiều cao tối đa của chồng cắt - ruột (CM)<br>
{{< katex >}}\mathcal{C}\mathscr{i}DetKnifePhase_{content}{{< /katex >}}: Thời gian chuẩn bị và cắt một nhát - ruột (Phút/Chồng)<br>

  {{< /details >}}
- **Gấp sách**
  * *Công thức tính thời gian gấp sách*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGGS
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Folding{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{(N_t * 60) / \mathcal{C}\mathscr{i}Det_{Foldingmachinefin}}\rceil + \lceil{p_t/ i_t}\rceil * \mathcal{C}\mathscr{i}Det_{Foldingmachineprep}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}N_t{{< /katex >}}: Tổng tờ giấy ruột tiêu thụ (Tờ)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Foldingmachinefin}{{< /katex >}}: Tốc độ máy gấp sách (Tay sách/Giờ)<br>
{{< katex >}}p_t{{< /katex >}}: Số trang ruột khách hàng (Trang)<br>
{{< katex >}}i_t{{< /katex >}}: Kiểu bình ruột (Trang/tờ)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Foldingmachineprep}{{< /katex >}}: Thời gian chuẩn bị máy gấp sách (Phút)<br>

  {{< /details >}}
- **Bắt tay sách**
  * *Thời gian gom tay sách thành khối ruột*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGKBTS
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Collating{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(Q_g * 60) / \mathcal{C}\mathscr{i}Det_{Collating} + \mathcal{C}\mathscr{i}Prep_{Collating}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Collating}{{< /katex >}}: Tốc độ bắt tay sách (Cuốn/Giờ)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Prep_{Collating}{{< /katex >}}: Thời gian chuẩn bị bắt tay sách (Phút)<br>

  {{< /details >}}
- **Vào keo**
  * *Thời gian vào keo*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGVK
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Glue{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(Q_g * 60) / \mathcal{C}\mathscr{i}Det_{Glue} + \mathcal{C}\mathscr{i}Prep_{Glue}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Glue}{{< /katex >}}: Tốc độ dây chuyền đóng cuốn keo (Cuốn/Giờ)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Prep_{Glue}{{< /katex >}}: Thời gian setup và vệ sinh máy đóng cuốn keo (Phút)<br>

  {{< /details >}}
- **Xén 3 mặt**
  * *Thời gian xén 3 mặt*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGXEN
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Trim{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{(Q_g * 60) / \mathcal{C}\mathscr{i}Det_{Trim} + \mathcal{C}\mathscr{i}Prep_{Trim}}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q_g{{< /katex >}}: Số khối ruột cần sản xuất (Cuốn)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Trim}{{< /katex >}}: Tốc độ vào bìa, xén 3 mặt (Cuốn/Giờ)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Prep_{Trim}{{< /katex >}}: Thời gian chuẩn bị vào bìa, xén 3 mặt (Phút)<br>

  {{< /details >}}
- **Đóng gói**
  * *Thời gian đóng gói*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGDG
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Packaging{{< /katex >}}
  * *Công thức* :{{< katex >}}\lceil{\lceil{Q / \mathcal{C}\mathscr{i}NoBookPerPack}\rceil * \mathcal{C}\mathscr{i}Det_{Packaging} / \mathcal{C}\mathscr{i}NoPackWorker}\rceil{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}Q{{< /katex >}}: Số lượng thành phẩm (Cuốn)<br>
{{< katex >}}\mathcal{C}\mathscr{i}NoBookPerPack{{< /katex >}}: Số sách mỗi gói (Cuốn)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Det_{Packaging}{{< /katex >}}: Tốc độ đóng gói trung bình (Phút/Gói)<br>
{{< katex >}}\mathcal{C}\mathscr{i}NoPackWorker{{< /katex >}}: Số nhân công đóng gói (Người)<br>

  {{< /details >}}
- **Thời gian hoàn thiện khác**
  * *Thời gian hoàn thiện khác*
  * *Đơn vị*: Phút
  * *Mã*: CHRCMOTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{completion}{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{i}Other_{CompletionInput}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Other_{CompletionInput}{{< /katex >}}: Thời gian hoàn thiện khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian hoàn thiện**
  * *Toàn bộ thời gian hoàn thiện*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMCM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}COM{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}\mathscr{i}Lamination + \mathcal{C}\mathscr{i}KnifePhase_{cover} + \mathcal{C}\mathscr{i}KnifePhase_{content} + \mathcal{C}\mathscr{i}Folding + \mathcal{C}\mathscr{i}Collating + \mathcal{C}\mathscr{i}Sewing + \mathcal{C}\mathscr{i}Stapling + \mathcal{C}\mathscr{i}Glue + \mathcal{C}\mathscr{i}Covering + \mathcal{C}\mathscr{i}Trim + \mathcal{C}\mathscr{i}Packaging + \mathcal{C}\mathscr{i}Other_{completion}{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}\mathscr{i}Lamination{{< /katex >}}: Cán màng (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{cover}{{< /katex >}}: Pha cắt bìa (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{content}{{< /katex >}}: Pha cắt ruột (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Folding{{< /katex >}}: Gấp sách (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Collating{{< /katex >}}: Bắt tay sách (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Sewing{{< /katex >}}: Khâu chỉ (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Stapling{{< /katex >}}: Đóng ghim (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Glue{{< /katex >}}: Vào keo (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Covering{{< /katex >}}: Vào bìa (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Trim{{< /katex >}}: Xén 3 mặt (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Packaging{{< /katex >}}: Đóng gói (Phút)<br>
{{< katex >}}\mathcal{C}\mathscr{i}Other_{completion}{{< /katex >}}: Thời gian hoàn thiện khác (Phút)<br>

  {{< /details >}}
- **Tổng thời gian sản xuất**
  * *Toàn bộ thời gian sản xuất*
  * *Đơn vị*: Phút
  * *Mã*: CHRTTL
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}TOTAL{{< /katex >}}
  * *Công thức* :{{< katex >}}\mathcal{C}{\Sigma}PPR + \mathcal{C}{\Sigma}PRT + \mathcal{C}{\Sigma}COM{{< /katex >}}

  {{< details "Thành Phần" >}}{{< katex >}}\mathcal{C}{\Sigma}PPR{{< /katex >}}: Tổng thời gian chế bản (Phút)<br>
{{< katex >}}\mathcal{C}{\Sigma}PRT{{< /katex >}}: Tổng thời gian in (Phút)<br>
{{< katex >}}\mathcal{C}{\Sigma}COM{{< /katex >}}: Tổng thời gian hoàn thiện (Phút)<br>

  {{< /details >}}



