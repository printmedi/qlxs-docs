---
bookFlatSection: true
weight: 20
type: docs
title: Tham Số Nguyên Vật Liệu
url: /sach/material-input
---

# Tham Số Nguyên Vật Liệu Cho In Sách

Dưới đây là những tham số liên quan tới thiết lập nguyên vật liệu mà cần người dùng cần nhập để tạo đơn in Sách.

## Thông tin đầu vào chung
**Thông tin đầu vào được sử dụng bởi tất cả hình thức gia công**

- **Chiều dài thành phẩm**
  * *Chiều cao sách sau xén.*
  * *Đơn vị*: cm
  * *Mã*: MATKTPL
  * *Kí hiệu*: {{< katex >}}h{{< /katex >}}

- **Chiều rộng thành phẩm**
  * *Chiều ngang một trang sau xén.*
  * *Đơn vị*: cm
  * *Mã*: MATKTPW
  * *Kí hiệu*: {{< katex >}}w{{< /katex >}}

- **Số lượng thành phẩm**
  * *Số cuốn tốt cần giao.*
  * *Đơn vị*: Cuốn
  * *Mã*: MATCC
  * *Kí hiệu*: {{< katex >}}Q{{< /katex >}}

## Thông tin đầu vào bìa
**Thông tin đầu vào chỉ liên quan tới bìa**

- **Số trang bìa**
  * *Bìa mềm gồm bìa 1–4.*
  * *Đơn vị*: Trang
  * *Mã*: MATSPB
  * *Kí hiệu*: {{< katex >}}p_c{{< /katex >}}
  * *Tập giá trị*: •  4  	
- **Định lượng giấy bìa**
  * *Khối lượng trên một mét vuông giấy bìa.*
  * *Đơn vị*: g/m²
  * *Mã*: MATDLB
  * *Kí hiệu*: {{< katex >}}gsm_c{{< /katex >}}

- **Caliper giấy bìa**
  * *Độ dày đo được của một tờ giấy bìa.*
  * *Đơn vị*: µm
  * *Mã*: MATCALB
  * *Kí hiệu*: {{< katex >}}t_c{{< /katex >}}

- **Số màu in bìa**
  * *Số màu tách bản cho bìa.*
  * *Đơn vị*: Màu
  * *Mã*: MATNCLB
  * *Kí hiệu*: {{< katex >}}c_c{{< /katex >}}

- **Số mặt in bìa**
  * *Số mặt có in trên tờ bìa.*
  * *Đơn vị*: Mặt
  * *Mã*: MATNSDB
  * *Kí hiệu*: {{< katex >}}d_c{{< /katex >}}
  * *Tập giá trị*: •  1  	•  2  	
- **Độ phủ trung bình mỗi màu bìa**
  * *Phần trăm diện tích trung bình của mỗi màu trên mỗi mặt in.*
  * *Đơn vị*: %
  * *Mã*: MATCOVCOV
  * *Kí hiệu*: {{< katex >}}a_c{{< /katex >}}

- **Số mặt cán màng bìa**
  * *Số mặt tờ bìa được cán màng.*
  * *Đơn vị*: Mặt
  * *Mã*: MATLAMS
  * *Kí hiệu*: {{< katex >}}n_{lam}{{< /katex >}}
  * *Tập giá trị*: •  0  	•  1  	•  2  	
## Thông tin đầu vào ruột
**Thông tin đầu vào liên quan tới ruột**

- **Số trang ruột khách hàng**
  * *Số trang nội dung khách hàng giao, chưa gồm trang trắng bù tay.*
  * *Đơn vị*: Trang
  * *Mã*: MATSPR
  * *Kí hiệu*: {{< katex >}}p_t{{< /katex >}}

- **Định lượng giấy ruột**
  * *Khối lượng trên một mét vuông giấy ruột.*
  * *Đơn vị*: g/m²
  * *Mã*: MATDLR
  * *Kí hiệu*: {{< katex >}}gsm_t{{< /katex >}}

- **Caliper giấy ruột**
  * *Độ dày đo được của một tờ theo ISO 534; không suy ra từ định lượng.*
  * *Đơn vị*: µm
  * *Mã*: MATCALR
  * *Kí hiệu*: {{< katex >}}t_t{{< /katex >}}

- **Số màu in ruột**
  * *Số màu tách bản cho ruột.*
  * *Đơn vị*: Màu
  * *Mã*: MATNCLR
  * *Kí hiệu*: {{< katex >}}c_t{{< /katex >}}

- **Số mặt in ruột**
  * *Số mặt có in trên tờ ruột.*
  * *Đơn vị*: Mặt
  * *Mã*: MATNSDR
  * *Kí hiệu*: {{< katex >}}d_t{{< /katex >}}
  * *Tập giá trị*: •  1  	•  2  	
- **Độ phủ trung bình mỗi màu ruột**
  * *Phần trăm diện tích trung bình của mỗi màu trên mỗi mặt in.*
  * *Đơn vị*: %
  * *Mã*: MATCOVCON
  * *Kí hiệu*: {{< katex >}}a_t{{< /katex >}}

## Thông tin đầu vào thiết lập máy in
**Thông tin đầu vào liên quan tới thiết lập máy in**

- **Kiểu bình bìa**
  * *Số trang bìa sản xuất bởi một tờ in hai mặt; chọn theo sơ đồ bình thực tế.*
  * *Đơn vị*: Trang/tờ
  * *Mã*: MATKBB
  * *Kí hiệu*: {{< katex >}}i_c{{< /katex >}}
  * *Tập giá trị*: •  4  	•  8  	•  16  	•  32  	
- **Kiểu bình ruột**
  * *Số trang thành phẩm trong một tay sách/tờ in hai mặt.*
  * *Đơn vị*: Trang/tờ
  * *Mã*: MATKBR
  * *Kí hiệu*: {{< katex >}}i_t{{< /katex >}}
  * *Tập giá trị*: •  8  	•  16  	•  32  	
- **Khổ máy in bìa - dài**
  * *Kích thước tờ tối đa của máy theo trục dài.*
  * *Đơn vị*: cm
  * *Mã*: MATKMILCOV
  * *Kí hiệu*: {{< katex >}}M_{c,l}{{< /katex >}}

- **Khổ máy in bìa - rộng**
  * *Kích thước tờ tối đa của máy theo trục rộng.*
  * *Đơn vị*: cm
  * *Mã*: MATKMIWCOV
  * *Kí hiệu*: {{< katex >}}M_{c,w}{{< /katex >}}

- **Khổ máy in ruột - dài**
  * *Kích thước tờ tối đa của máy theo trục dài.*
  * *Đơn vị*: cm
  * *Mã*: MATKMILCON
  * *Kí hiệu*: {{< katex >}}M_{t,l}{{< /katex >}}

- **Khổ máy in ruột - rộng**
  * *Kích thước tờ tối đa của máy theo trục rộng.*
  * *Đơn vị*: cm
  * *Mã*: MATKMIWCON
  * *Kí hiệu*: {{< katex >}}M_{t,w}{{< /katex >}}

- **Khổ tờ chạy bìa - dài**
  * *Chiều dài tờ giấy thực tế đưa vào máy.*
  * *Đơn vị*: cm
  * *Mã*: MATKLTCOV
  * *Kí hiệu*: {{< katex >}}S_{c,l}{{< /katex >}}

- **Khổ tờ chạy bìa - rộng**
  * *Chiều rộng tờ giấy thực tế đưa vào máy.*
  * *Đơn vị*: cm
  * *Mã*: MATKWTCOV
  * *Kí hiệu*: {{< katex >}}S_{c,w}{{< /katex >}}

- **Khổ tờ chạy ruột - dài**
  * *Chiều dài tờ giấy thực tế đưa vào máy.*
  * *Đơn vị*: cm
  * *Mã*: MATKLTCON
  * *Kí hiệu*: {{< katex >}}S_{t,l}{{< /katex >}}

- **Khổ tờ chạy ruột - rộng**
  * *Chiều rộng tờ giấy thực tế đưa vào máy.*
  * *Đơn vị*: cm
  * *Mã*: MATKWTCON
  * *Kí hiệu*: {{< katex >}}S_{t,w}{{< /katex >}}

- **Khổ bản bìa - dài**
  * *Chiều dài bản offset bìa.*
  * *Đơn vị*: cm
  * *Mã*: MATKPLTCOV
  * *Kí hiệu*: {{< katex >}}B_{c,l}{{< /katex >}}

- **Khổ bản bìa - rộng**
  * *Chiều rộng bản offset bìa.*
  * *Đơn vị*: cm
  * *Mã*: MATKPWTCOV
  * *Kí hiệu*: {{< katex >}}B_{c,w}{{< /katex >}}

- **Khổ bản ruột - dài**
  * *Chiều dài bản offset ruột.*
  * *Đơn vị*: cm
  * *Mã*: MATKPLTCON
  * *Kí hiệu*: {{< katex >}}B_{t,l}{{< /katex >}}

- **Khổ bản ruột - rộng**
  * *Chiều rộng bản offset ruột.*
  * *Đơn vị*: cm
  * *Mã*: MATKPWTCON
  * *Kí hiệu*: {{< katex >}}B_{t,w}{{< /katex >}}

## Thông tin đầu vào khác
**Thông tin đầu vào khác**

- **Tỷ lệ trang chữ trên trang ảnh**
  * *Chỉ dùng ước lượng thời gian tiền kỳ.*
  * *Đơn vị*: Hệ số
  * *Mã*: MATTLC
  * *Kí hiệu*: {{< katex >}}r{{< /katex >}}

- **Độ dày màng keo gáy**
  * *Độ dày lớp keo gáy hiệu lực; profile cung cấp bootstrap, nhà máy phải thay theo TDS và cài đặt đầu phun/con lăn.*
  * *Đơn vị*: mm
  * *Mã*: MATGLUET
  * *Kí hiệu*: {{< katex >}}t_{glue}{{< /katex >}}

- **Chiều sâu phay gáy**
  * *Phần kích thước ruột bị loại ở mép gáy để mở xơ giấy; phải lấy từ recipe máy và sơ đồ bình.*
  * *Đơn vị*: cm
  * *Mã*: MATMILLDEPTH
  * *Kí hiệu*: {{< katex >}}d_{mill}{{< /katex >}}

- **Lượng dư xén đầu/chân mỗi đầu**
  * *Phần dư ở đầu và chân sách trước xén, dùng tính chiều dài đường keo thực tế.*
  * *Đơn vị*: cm
  * *Mã*: MATHEADTRIM
  * *Kí hiệu*: {{< katex >}}a_{trim}{{< /katex >}}

- **Khối lượng riêng keo gáy**
  * *Khối lượng riêng dùng đổi thể tích màng keo sang khối lượng.*
  * *Đơn vị*: g/cm³
  * *Mã*: MATGLUEDENS
  * *Kí hiệu*: {{< katex >}}rho_{glue}{{< /katex >}}

- **Định mức keo hông EVA theo chiều dài**
  * *Khối lượng keo hông cho một mét đường keo trên một bên gáy.*
  * *Đơn vị*: g/m
  * *Mã*: MATGLUESIDE
  * *Kí hiệu*: {{< katex >}}m_{side}{{< /katex >}}

- **Tỷ lệ hao hụt keo gáy**
  * *Hao hụt keo gáy do mồi hệ thống, vệ sinh, tồn dư và phế phẩm.*
  * *Đơn vị*: Hệ số
  * *Mã*: MATGLUELOSSSP
  * *Kí hiệu*: {{< katex >}}w_{glue,spine}{{< /katex >}}

- **Tỷ lệ hao hụt keo hông**
  * *Hao hụt riêng của hệ thống keo hông EVA.*
  * *Đơn vị*: Hệ số
  * *Mã*: MATGLUELOSSSI
  * *Kí hiệu*: {{< katex >}}w_{glue,side}{{< /katex >}}

- **Đơn giá keo gáy**
  * *Giá mua hiệu lực của keo gáy theo profile được chọn.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: MATGLUEPRSP
  * *Kí hiệu*: {{< katex >}}c_{glue,spine}{{< /katex >}}

- **Đơn giá keo hông EVA**
  * *Giá mua hiệu lực của keo hông EVA.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: MATGLUEPRSI
  * *Kí hiệu*: {{< katex >}}c_{glue,side}{{< /katex >}}

- **Độ dày keo gáy tối thiểu theo recipe**
  * *Giới hạn dưới theo TDS và cấu hình đầu bôi keo.*
  * *Đơn vị*: mm
  * *Mã*: MATGLUEMIN
  * *Kí hiệu*: {{< katex >}}t_{glue,min}{{< /katex >}}

- **Độ dày keo gáy tối đa theo recipe**
  * *Giới hạn trên theo TDS và cấu hình đầu bôi keo.*
  * *Đơn vị*: mm
  * *Mã*: MATGLUEMAX
  * *Kí hiệu*: {{< katex >}}t_{glue,max}{{< /katex >}}

- **Thời gian chờ đạt điều kiện QC keo**
  * *Thời gian chờ ngoài máy trước mốc QC/release; không cộng vào thời gian chiếm dụng dây chuyền.*
  * *Đơn vị*: Giờ
  * *Mã*: MATGLUEWAIT
  * *Kí hiệu*: {{< katex >}}t_{qc}{{< /katex >}}

- **Số ghim mỗi cuốn**
  * *Số ghim thực tế dọc đường gấp giữa; không được vượt số đầu ghim khả dụng của máy.*
  * *Đơn vị*: Ghim/Cuốn
  * *Mã*: MATSTITCHCOUNT
  * *Kí hiệu*: {{< katex >}}n_{stitch}{{< /katex >}}

- **Chiều dài dây cho mỗi ghim**
  * *Chiều dài dây máy cắt để tạo một ghim; phải chỉnh theo độ dày tập lồng và xác nhận bằng ghim thử.*
  * *Đơn vị*: mm/Ghim
  * *Mã*: MATWIRELEN
  * *Kí hiệu*: {{< katex >}}l_{wire}{{< /katex >}}

- **Khối lượng dây ghim trên mét**
  * *Khối lượng một mét dây theo đúng đường kính, lớp phủ và lô vật tư đang dùng.*
  * *Đơn vị*: g/m
  * *Mã*: MATWIREMASS
  * *Kí hiệu*: {{< katex >}}m_{wire/m}{{< /katex >}}

- **Tỷ lệ hao hụt dây ghim**
  * *Hao hụt do setup, ghim thử, cắt lỗi, loại sản phẩm và dây tồn trên đường cấp.*
  * *Đơn vị*: Hệ số
  * *Mã*: MATWIRELOSS
  * *Kí hiệu*: {{< katex >}}w_{wire}{{< /katex >}}

- **Đơn giá dây ghim**
  * *Giá mua hiệu lực của đúng loại dây ghim.*
  * *Đơn vị*: VNĐ/kg
  * *Mã*: MATWIREPRICE
  * *Kí hiệu*: {{< katex >}}c_{wire}{{< /katex >}}

- **Độ dày cuốn đóng ghim tối đa**
  * *Giới hạn tổng độ dày cuốn đã gồm hai lớp bìa theo cấu hình máy/dây chuyền.*
  * *Đơn vị*: mm
  * *Mã*: MATSTITCHTHICKMAX
  * *Kí hiệu*: {{< katex >}}t_{book,max}{{< /katex >}}

- **Số trạm cấp tay tối đa**
  * *Số tay ruột khác nhau tối đa có thể cấp trong một lượt chạy cấu hình hiện tại.*
  * *Đơn vị*: Trạm
  * *Mã*: MATSTITCHFEEDMAX
  * *Kí hiệu*: {{< katex >}}n_{feeder,max}{{< /katex >}}

- **Số đầu ghim khả dụng tối đa**
  * *Số đầu ghim đang lắp và được phép dùng đồng thời trên cấu hình máy.*
  * *Đơn vị*: Đầu ghim
  * *Mã*: MATSTITCHHEADMAX
  * *Kí hiệu*: {{< katex >}}n_{head,max}{{< /katex >}}

- **Khổ thành phẩm đóng ghim - rộng tối thiểu**
  * *Giới hạn chiều rộng thành phẩm của dây chuyền đóng ghim.*
  * *Đơn vị*: cm
  * *Mã*: MATSTITCHWMIN
  * *Kí hiệu*: {{< katex >}}W_{stitch,min}{{< /katex >}}

- **Khổ thành phẩm đóng ghim - rộng tối đa**
  * *Giới hạn chiều rộng thành phẩm của dây chuyền đóng ghim.*
  * *Đơn vị*: cm
  * *Mã*: MATSTITCHWMAX
  * *Kí hiệu*: {{< katex >}}W_{stitch,max}{{< /katex >}}

- **Khổ thành phẩm đóng ghim - dài tối thiểu**
  * *Giới hạn chiều dài thành phẩm của dây chuyền đóng ghim.*
  * *Đơn vị*: cm
  * *Mã*: MATSTITCHHMIN
  * *Kí hiệu*: {{< katex >}}H_{stitch,min}{{< /katex >}}

- **Khổ thành phẩm đóng ghim - dài tối đa**
  * *Giới hạn chiều dài thành phẩm của dây chuyền đóng ghim.*
  * *Đơn vị*: cm
  * *Mã*: MATSTITCHHMAX
  * *Kí hiệu*: {{< katex >}}H_{stitch,max}{{< /katex >}}



