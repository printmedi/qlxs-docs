---
bookFlatSection: true
weight: 50
type: docs
title: Tính Toán Thời Gian
url: /bao_bi/chrono-calculate
---

# Kết Quả Tính Toán Thời Gian Cho In Bao bì hộp

Dưới đây là những kết quả tính toán liên quan tới giá trị thời gian cho đơn in Bao bì hộp.

## Thời gian chế bản
**Bình bản, RIP, ghi bản và in thử**

- **Bình bản hộp**
  * *Bình một form khuôn hộp lên khổ tờ candidate đã chọn.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTIMPOSE
  * *Kí hiệu*: {{< katex >}}T_i{{< /katex >}}

- **RIP hộp**
  * *Một form hộp cho mỗi mặt in; tốc độ RIP tính theo mặt artwork.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTRIP
  * *Kí hiệu*: {{< katex >}}T_r{{< /katex >}}

- **Ghi hiện bản hộp**
  * *Mỗi màu trên mỗi mặt cần một bản offset riêng.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPLATE
  * *Kí hiệu*: {{< katex >}}T_p{{< /katex >}}

- **In thử hộp**
  * *Proof một trang cho mỗi mặt artwork, cộng thời gian chuẩn bị thiết bị.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPROOF
  * *Kí hiệu*: {{< katex >}}T_t{{< /katex >}}

- **Tổng thời gian chế bản**
  * *Bình bản, RIP, ghi hiện toàn bộ bản offset và in thử.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPREPRESS
  * *Kí hiệu*: {{< katex >}}T_{pre}{{< /katex >}}

## Thời gian in
**Setup bản và chạy máy offset tờ rời**

- **Chạy in hộp**
  * *Tổng tờ chạy nhân số lượt pass theo khả năng máy.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRINT
  * *Kí hiệu*: {{< katex >}}T_{run}{{< /katex >}}

- **Căn chỉnh in hộp**
  * *Số bản nhân thời gian setup mỗi bản.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTSETUP
  * *Kí hiệu*: {{< katex >}}T_s{{< /katex >}}

- **Tổng thời gian in**
  * *Chạy máy cộng căn chỉnh bản.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRINTTOTAL
  * *Kí hiệu*: {{< katex >}}T_{print}{{< /katex >}}

## Thời gian hoàn thiện
**Pha cắt, bế/cấn/tách phế, gấp-dán và đóng gói**

- **Pha cắt tờ hộp**
  * *Chia tổng tờ cần chạy thành chồng theo caliper rồi nhân số nhát cắt mỗi chồng; bằng 0 nếu tờ đã đúng khổ.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPRECUT
  * *Kí hiệu*: {{< katex >}}T_c{{< /katex >}}

- **Bế, cấn và tách phế hộp**
  * *Chạy số tờ tốt qua máy bế/cấn có bộ phận tách phế, cộng setup khuôn và register.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTDIECUT
  * *Kí hiệu*: {{< katex >}}T_d{{< /katex >}}

- **Gấp và dán hộp**
  * *Gấp đường cấn, bôi keo tai dán và ép đường dán trên folder-gluer.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTGLUE
  * *Kí hiệu*: {{< katex >}}T_g{{< /katex >}}

- **Đóng gói hộp phẳng**
  * *Bó hoặc đóng gói đủ sản lượng giao sau gấp dán.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTPACK
  * *Kí hiệu*: {{< katex >}}T_b{{< /katex >}}

- **Tổng thời gian hoàn thiện**
  * *Pha cắt tờ, bế/cấn/tách phế, gấp-dán và đóng gói hộp phẳng.*
  * *Đơn vị*: Phút
  * *Mã*: BBCTFINISH
  * *Kí hiệu*: {{< katex >}}T_{finish}{{< /katex >}}



