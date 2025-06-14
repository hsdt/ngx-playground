# hs-phong-giuong-picker

`<hs-phong-giuong-picker>` là một component dùng để mở popup và cập nhật thông tin số buồng và số giường, cho phép mở popup chọn buồng/giường bằng thao tác double-click.

| Thuộc tính       | Kiểu dữ liệu | Mặc định | Mô tả                                                 |
|------------------|--------------|----------|-------------------------------------------------------|
| `soPhong`        | string       | `''`     | Giá trị số buồng hiện tại                             |
| `soPhongUpdate`  | string       | `''`     | Tên trường dữ liệu sẽ cập nhật khi thay đổi số buồng  |
| `soGiuong`       | string       | `''`     | Giá trị số giường hiện tại                            |
| `soGiuongUpdate` | string       | `''`     | Tên trường dữ liệu sẽ cập nhật khi thay đổi số giường |
| `style`          | string       | `''`     | Inline style cho element                              |
| `class`          | string       | `''`     | Class CSS cho element                                 |

> 💡 Khi double-click vào component, kích hoạt mở popup chọn phòng giường.

Example:

```html
<hs-phong-giuong-picker
  [soPhong]="context.tempData.hsBenhAn.SoPhong"
  soPhongUpdate="tempData.hsBenhAn.SoPhong"
  [soGiuong]="context.tempData.hsBenhAn.SoGiuong"
  soGiuongUpdate="tempData.hsBenhAn.SoGiuong"
></hs-phong-giuong-picker>
