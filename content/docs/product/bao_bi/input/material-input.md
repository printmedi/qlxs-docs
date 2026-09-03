---
bookFlatSection: true
weight: 20
type: docs
title: Tham Số Nguyên Vật Liệu
url: /bao_bi/material-input
---

# Tham Số Nguyên Vật Liệu Cho In Bao bì hộp

Dưới đây là những tham số liên quan tới thiết lập nguyên vật liệu mà cần người dùng cần nhập để tạo đơn in Bao bì hộp.

## Thông tin hộp thành phẩm
**Sản lượng và ba kích thước thành phẩm**

- **Số lượng hộp cần giao**
  * *Số hộp tốt khách hàng yêu cầu.*
  * *Đơn vị*: Hộp
  * *Mã*: BBINQTY
  * *Kí hiệu*: {{< katex >}}Q{{< /katex >}}

- **Chiều dài hộp**
  * *Chiều dài thành phẩm sau gấp.*
  * *Đơn vị*: mm
  * *Mã*: BBINLENGTH
  * *Kí hiệu*: {{< katex >}}L{{< /katex >}}

- **Chiều rộng hộp**
  * *Chiều rộng thành phẩm sau gấp.*
  * *Đơn vị*: mm
  * *Mã*: BBINWIDTH
  * *Kí hiệu*: {{< katex >}}W{{< /katex >}}

- **Chiều cao hộp**
  * *Chiều cao thân hộp sau gấp.*
  * *Đơn vị*: mm
  * *Mã*: BBINHEIGHT
  * *Kí hiệu*: {{< katex >}}H{{< /katex >}}

## Giấy hộp
**Giấy/carton dùng cho hộp**

- **Định lượng giấy hộp**
  * *Tự điền từ catalog giấy đã chọn.*
  * *Đơn vị*: g/m²
  * *Mã*: BBINGSM
  * *Kí hiệu*: {{< katex >}}G{{< /katex >}}

- **Độ dày giấy hộp**
  * *Caliper thực của mã giấy, không suy từ GSM; engine chỉ dùng khi profile có bù đường cấn.*
  * *Đơn vị*: µm
  * *Mã*: BBINCALIPER
  * *Kí hiệu*: {{< katex >}}t{{< /katex >}}

## Không sử dụng
**Section tương thích schema; Bao bì không có ruột sách**

## Candidate tờ in và nesting
**Một phương án cụ thể do engine dựng và kiểm tra**

- **Khổ tờ chạy - dài**
  * *Chiều dài tờ candidate do engine gửi.*
  * *Đơn vị*: cm
  * *Mã*: BBINSHEETL
  * *Kí hiệu*: {{< katex >}}S_L{{< /katex >}}

- **Khổ tờ chạy - rộng**
  * *Chiều rộng tờ candidate do engine gửi.*
  * *Đơn vị*: cm
  * *Mã*: BBINSHEETW
  * *Kí hiệu*: {{< katex >}}S_W{{< /katex >}}

- **Số hộp trên một tờ**
  * *Số polygon hộp engine đã đặt thành công trên một tờ.*
  * *Đơn vị*: Hộp/Tờ
  * *Mã*: BBINPERSHEET
  * *Kí hiệu*: {{< katex >}}N_s{{< /katex >}}

- **Diện tích khuôn phẳng một hộp**
  * *Diện tích polygon khuôn phẳng do engine dựng, không phải hình chữ nhật bao ngoài.*
  * *Đơn vị*: mm²
  * *Mã*: BBINDIEAREA
  * *Kí hiệu*: {{< katex >}}A_d{{< /katex >}}

- **Số nhát pha cắt mỗi chồng**
  * *Số nhát máy dao cần thực hiện trên mỗi chồng để đưa tờ nguyên liệu về khổ chạy; nhập 0 nếu vật liệu đã đúng khổ.*
  * *Đơn vị*: Nhát/Chồng
  * *Mã*: BBINCUTSPERPILE
  * *Kí hiệu*: {{< katex >}}N_c{{< /katex >}}

- **Khổ máy in - dài**
  * *Kích thước tờ tối đa máy in tiếp nhận.*
  * *Đơn vị*: cm
  * *Mã*: BBINMACHINEL
  * *Kí hiệu*: {{< katex >}}M_L{{< /katex >}}

- **Khổ máy in - rộng**
  * *Kích thước tờ tối đa máy in tiếp nhận.*
  * *Đơn vị*: cm
  * *Mã*: BBINMACHINEW
  * *Kí hiệu*: {{< katex >}}M_W{{< /katex >}}

## Thông tin in
**Màu, mặt in và độ phủ mực**

- **Số màu in hộp**
  * *Số màu/bản offset của artwork.*
  * *Đơn vị*: Màu
  * *Mã*: BBINCOLORS
  * *Kí hiệu*: {{< katex >}}C{{< /katex >}}

- **Số mặt in hộp**
  * *Số mặt tờ cần in.*
  * *Đơn vị*: Mặt
  * *Mã*: BBINSIDES
  * *Kí hiệu*: {{< katex >}}D{{< /katex >}}
  * *Tập giá trị*: •  1  	•  2  	
- **Độ phủ trung bình mỗi màu**
  * *Độ phủ trung bình của một màu trên diện tích tờ chạy.*
  * *Đơn vị*: %
  * *Mã*: BBINCOVERAGE
  * *Kí hiệu*: {{< katex >}}a{{< /katex >}}



