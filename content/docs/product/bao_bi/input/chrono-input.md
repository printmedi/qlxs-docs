---
bookFlatSection: true
weight: 30
type: docs
title: Tham Số Thời Gian
url: /bao_bi/chrono-input
---

# Tham Số Thời Gian Cho In Bao bì hộp

Dưới đây là những tham số liên quan tới thiết lập thời gian mà cần người dùng cần nhập để tạo đơn in Bao bì hộp.

## Thông số thời gian máy
**Tốc độ, khổ và thời gian setup lấy từ các máy trong dây chuyền**

- **Thời gian bình bản hộp**
  * *Thời gian planning để bình một form hộp lên tờ chạy đã chọn.*
  * *Đơn vị*: Phút
  * *Mã*: BBCIPREIMPOSE
  * *Kí hiệu*: {{< katex >}}t_i{{< /katex >}}

- **Tốc độ RIP hộp**
  * *Số mặt artwork hộp RIP được trong một phút.*
  * *Đơn vị*: Mặt/Phút
  * *Mã*: BBCIPRERIP
  * *Kí hiệu*: {{< katex >}}v_r{{< /katex >}}

- **Thời gian ghi hiện mỗi bản hộp**
  * *Số phút để ghi và hiện một bản offset.*
  * *Đơn vị*: Phút/Bản
  * *Mã*: BBCIPREPLATE
  * *Kí hiệu*: {{< katex >}}t_p{{< /katex >}}

- **Tốc độ in thử hộp**
  * *Số trang proof một mặt hoàn thành trong một phút.*
  * *Đơn vị*: Trang/phút
  * *Mã*: BBCIPREPROOFSPD
  * *Kí hiệu*: {{< katex >}}v_t{{< /katex >}}

- **Thời gian chuẩn bị in thử hộp**
  * *Thời gian mở file, nạp vật liệu và chuẩn bị thiết bị proof.*
  * *Đơn vị*: Phút
  * *Mã*: BBCIPREPROOFSETUP
  * *Kí hiệu*: {{< katex >}}t_t{{< /katex >}}

- **Thời gian một nhát pha cắt hộp**
  * *Phút để xếp chồng và chém một nhát trên máy dao.*
  * *Đơn vị*: Phút/Chồng
  * *Mã*: BBCICUTTIME
  * *Kí hiệu*: {{< katex >}}t_c{{< /katex >}}

- **Chiều cao chồng pha cắt hộp**
  * *Chiều cao chồng tối đa máy dao giữ được.*
  * *Đơn vị*: CM
  * *Mã*: BBCICUTPILE
  * *Kí hiệu*: {{< katex >}}h_c{{< /katex >}}

- **Tốc độ planning máy in hộp**
  * *Tốc độ tờ/giờ thực tế sau hiệu chỉnh theo máy và job.*
  * *Đơn vị*: Tờ/Giờ
  * *Mã*: BBCIPRESSSPEED
  * *Kí hiệu*: {{< katex >}}v{{< /katex >}}

- **Số màu máy in hỗ trợ**
  * *Số màu máy in được trong một pass.*
  * *Đơn vị*: Màu
  * *Mã*: BBCIPRESSCOLORS
  * *Kí hiệu*: {{< katex >}}C_m{{< /katex >}}

- **Số mặt máy in hỗ trợ**
  * *Số mặt máy in được trong một pass.*
  * *Đơn vị*: Mặt
  * *Mã*: BBCIPRESSSIDES
  * *Kí hiệu*: {{< katex >}}D_m{{< /katex >}}
  * *Tập giá trị*: •  1  	•  2  	
- **Thời gian căn chỉnh mỗi bản hộp**
  * *Thời gian lắp bản, canh màu và register cho mỗi bản.*
  * *Đơn vị*: Phút/Bản
  * *Mã*: BBCIPRESSSETUP
  * *Kí hiệu*: {{< katex >}}T_s{{< /katex >}}

- **Tốc độ planning máy bế hộp**
  * *Năng suất bế/cấn và tách phế theo số tờ tốt mỗi giờ.*
  * *Đơn vị*: Tờ/Giờ
  * *Mã*: BBCIDIESPEED
  * *Kí hiệu*: {{< katex >}}v_d{{< /katex >}}

- **Thời gian chuẩn bị máy bế hộp**
  * *Lắp khuôn, căn chỉnh register, áp lực bế và bộ phận tách phế.*
  * *Đơn vị*: Phút
  * *Mã*: BBCIDIESETUP
  * *Kí hiệu*: {{< katex >}}t_d{{< /katex >}}

- **Khổ máy bế - dài**
  * *Chiều dài tờ tối đa máy bế tiếp nhận.*
  * *Đơn vị*: cm
  * *Mã*: BBCIDIELONG
  * *Kí hiệu*: {{< katex >}}D_L{{< /katex >}}

- **Khổ máy bế - rộng**
  * *Chiều rộng tờ tối đa máy bế tiếp nhận.*
  * *Đơn vị*: cm
  * *Mã*: BBCIDIEWIDE
  * *Kí hiệu*: {{< katex >}}D_W{{< /katex >}}

- **Tốc độ planning máy gấp dán hộp**
  * *Số hộp được gấp, bôi keo và ép đường dán trong một giờ planning.*
  * *Đơn vị*: Hộp/Giờ
  * *Mã*: BBCIGLUERSPEED
  * *Kí hiệu*: {{< katex >}}v_g{{< /katex >}}

- **Thời gian chuẩn bị máy gấp dán hộp**
  * *Setup feeder, dây đai, súng keo, cơ cấu gấp và bộ đếm theo kiểu hộp.*
  * *Đơn vị*: Phút
  * *Mã*: BBCIGLUERSETUP
  * *Kí hiệu*: {{< katex >}}t_g{{< /katex >}}

- **Số hộp mỗi gói**
  * *Số hộp phẳng thành phẩm được bó hoặc đóng trong một gói vận chuyển.*
  * *Đơn vị*: Hộp
  * *Mã*: BBCIPACKCOUNT
  * *Kí hiệu*: {{< katex >}}N_b{{< /katex >}}

- **Thời gian đóng một gói hộp**
  * *Số phút một nhân công cần cho một gói hộp phẳng.*
  * *Đơn vị*: Phút/Gói
  * *Mã*: BBCIPACKTIME
  * *Kí hiệu*: {{< katex >}}t_b{{< /katex >}}

- **Nhân công đóng gói hộp**
  * *Số người cùng tham gia đóng gói thành phẩm.*
  * *Đơn vị*: Người
  * *Mã*: BBCIPACKWORKERS
  * *Kí hiệu*: {{< katex >}}n_b{{< /katex >}}

- **Thời gian hoàn thiện khác**
  * *Ô nhập tay cho các khâu hoàn thiện chưa được mô hình hoá (cán màng, phủ UV, ép nhũ, dán cửa sổ, dán tay...).*
  * *Đơn vị*: Phút
  * *Mã*: BBCIOTHER
  * *Kí hiệu*: {{< katex >}}T_{other}{{< /katex >}}



