# Mẫu ví dụ đơn giản nhất

Một mẫu phiếu sau đây chỉ đơn giản là tạo ra một mẫu phiếu và chỉ có một ô nhập hiển thị `Tên bệnh nhân`.

```html
<hoso-page>
  <hs-input-text [value]="context.BenhNhan.HoTen" update="BenhNhan.HoTen"></hs-input-text>
</hoso-page>
```

## Thẻ: hoso-page

Thuộc tính: N/A

## Thẻ: hs-input-text

Thuộc tính:

* [value]: Giá trị mà thẻ sẽ đọc từ dữ liệu để hiện thị vào ô nhập.
* [update]: Tên trường dữ liệu sẽ được cập nhật khi có thay đổi.
* (valueChange): Sự kiện khi dữ liệu có thay đổi.
