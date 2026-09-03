---
bookFlatSection: true
weight: 50
type: docs
title: Tính Toán Thời Gian
url: /sach/chrono-calculate
---

# Kết Quả Tính Toán Thời Gian Cho In Sách

Dưới đây là những kết quả tính toán liên quan tới giá trị thời gian cho đơn in Sách.

## Thời gian chế bản
**Tính toán thời gian chế bản**

- **Soát lỗi, kiểm tra file chữ**
  * *Thời gian soát lỗi, kiểm tra file chữ*
  * *Đơn vị*: Phút
  * *Mã*: CHRKTT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{txt}{{< /katex >}}

- **Xử lý ảnh, kiểm tra file ảnh**
  * *Thời gian xử lý ảnh, kiểm tra file ảnh*
  * *Đơn vị*: Phút
  * *Mã*: CHRKTI
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Ktr_{img}{{< /katex >}}

- **Dàn trang**
  * *Thời gian dàn trang (layout)*
  * *Đơn vị*: Phút
  * *Mã*: CHRTDT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}T_{layout}{{< /katex >}}

- **Bình bản**
  * *Thời gian bình bản (Makeready)*
  * *Đơn vị*: Phút
  * *Mã*: CHRTBB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}Makeready{{< /katex >}}

- **In thử**
  * *Thời gian in thử*
  * *Đơn vị*: Phút
  * *Mã*: CHRTIT
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}test_print{{< /katex >}}

- **RIP**
  * *Thời gian RIP (Raster Image Processor).*
  * *Đơn vị*: Phút
  * *Mã*: CHRTRIP
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}rip{{< /katex >}}

- **Ghi hiện bản**
  * *Thời gian ghi hiện bản (Platemaking).*
  * *Đơn vị*: Phút
  * *Mã*: CHRTPLM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pp}platemaking{{< /katex >}}

- **Thời gian chế bản khác**
  * *Thời gian chế bản khác.*
  * *Đơn vị*: Phút
  * *Mã*: CHRDOTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{preprocessing}{{< /katex >}}

- **Tổng thời gian chế bản**
  * *Toàn bộ thời gian chế bản*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMPP
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}PPR{{< /katex >}}

## Thời gian in
**Tính toán thời gian in**

- **In bìa**
  * *Thời gian in bìa trong quá trình sản xuất*
  * *Đơn vị*: Phút
  * *Mã*: CHRPRCOV
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}P_{cover}{{< /katex >}}

- **In ruột**
  * *Thời gian in ruột trong quá trình sản xuất*
  * *Đơn vị*: Phút
  * *Mã*: CHRPRCON
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}P_{content}{{< /katex >}}

- **Căn chỉnh in bìa**
  * *Thời gian make-ready máy in cho bìa (lắp bản, canh mực, canh chồng màu). Tách riêng khỏi thời gian chạy in; = số bản in × phút mỗi bản (số bản = khuôn × màu × mặt).*
  * *Đơn vị*: Phút
  * *Mã*: CHRCCINB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}Mk_{cover}{{< /katex >}}

- **Căn chỉnh in ruột**
  * *Thời gian make-ready máy in cho ruột (lắp bản, canh mực, canh chồng màu). Tách riêng khỏi thời gian chạy in; = số bản in × phút mỗi bản (số bản = khuôn × màu × mặt).*
  * *Đơn vị*: Phút
  * *Mã*: CHRCCINR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{pr}Mk_{content}{{< /katex >}}

- **Thời gian in khác**
  * *Thời gian in khác.*
  * *Đơn vị*: Phút
  * *Mã*: CHRPROTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{printing}{{< /katex >}}

- **Tổng thời gian in**
  * *Toàn bộ thời gian in*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMPR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}PRT{{< /katex >}}

## Thời gian hoàn thiện
**Tính toán thời gian hoàn thiện**

- **Cán màng**
  * *Công thức tính thời gian cán màng*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGCM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Lamination{{< /katex >}}

- **Pha cắt bìa**
  * *Công thức tính thời gian pha cắt bìa*
  * *Đơn vị*: Phút
  * *Mã*: CHRKFPB
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{cover}{{< /katex >}}

- **Pha cắt ruột**
  * *Công thức tính thời gian pha cắt ruột*
  * *Đơn vị*: Phút
  * *Mã*: CHRKFPR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}KnifePhase_{content}{{< /katex >}}

- **Gấp sách**
  * *Công thức tính thời gian gấp sách*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGGS
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Folding{{< /katex >}}

- **Bắt tay sách**
  * *Thời gian gom tay sách thành khối ruột*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGKBTS
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Collating{{< /katex >}}

- **Khâu chỉ**
  * *Công thức tính thời gian khâu chỉ*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGKC
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Sewing{{< /katex >}}

- **Đóng ghim**
  * *Công thức tính thời gian đóng ghim*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGH
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Stapling{{< /katex >}}

- **Vào keo**
  * *Thời gian vào keo*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGVK
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Glue{{< /katex >}}

- **Vào bìa**
  * *Thời gian bôi keo gáy và vào bìa cho ruột đã khâu chỉ*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGV
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Covering{{< /katex >}}

- **Xén 3 mặt**
  * *Thời gian xén 3 mặt*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGXEN
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Trim{{< /katex >}}

- **Đóng gói**
  * *Thời gian đóng gói*
  * *Đơn vị*: Phút
  * *Mã*: CHRTGDG
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Packaging{{< /katex >}}

- **Thời gian hoàn thiện khác**
  * *Thời gian hoàn thiện khác*
  * *Đơn vị*: Phút
  * *Mã*: CHRCMOTHR
  * *Kí hiệu*: {{< katex >}}\mathcal{C}\mathscr{i}Other_{completion}{{< /katex >}}

- **Tổng thời gian hoàn thiện**
  * *Toàn bộ thời gian hoàn thiện*
  * *Đơn vị*: Phút
  * *Mã*: CHRSMCM
  * *Kí hiệu*: {{< katex >}}\mathcal{C}{\Sigma}COM{{< /katex >}}



