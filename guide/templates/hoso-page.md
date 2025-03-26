# hoso-page

> Khung nội dung mẫu phiếu, thiết lập các layout khổ giấy.

Thuộc tính: N/A

Ví dụ:

```html
<hoso-page>
  <hs tag="span" [text]="context.BenhAnChiTiet.CoSoTrucThuoc"></hs>
  <br>
  <hs tag="span" [text]="context.BenhAnChiTiet.TenBenhVien"></hs>
  <br>
  <hs-input-text [value]="context.BenhNhan.HoTen" update="BenhNhan.HoTen"></hs-input-text>
</hoso-page>
```

Diễn giải:

Một mẫu phiếu trên chỉ đơn giản là tạo ra một mẫu hiển thị các nội dung:

- Thẻ <span> hiển thị ` Tên cơ sở trực thuộc`
- Thẻ <span> hiển thị ` Tên bệnh viện`
- Một ô nhập hiển thị `Tên bệnh nhân`