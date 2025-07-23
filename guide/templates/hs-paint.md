# hs-paint

`<hs-paint>` là một component cho phép người dùng vẽ trực tiếp lên ảnh nền bằng chuột hoặc cảm ứng. Nó hỗ trợ các chức năng như chọn màu, xóa (tẩy), chọn ảnh từ thiết bị, hoặc từ danh mục dữ liệu.

| Thuộc tính     | Kiểu dữ liệu | Mặc định                      | Mô tả                                               |
|----------------|--------------|-------------------------------|-----------------------------------------------------|
| `value`        | string       | `''`                          | Data URL hoặc đường dẫn ảnh hiện tại                |
| `defaultValue` | string       | `'assets/img/TaiMuiHong.png'` | Ảnh nền mặc định khi `value` trống                  |
| `update`       | string       | `''`                          | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `style`        | string       | `''`                          | Inline style cho component                          |
| `class`        | string       | `''`                          | Class CSS cho component                             |
| `lineColor`    | string       | `'#F00'`                      | Mã màu nét vẽ                                       |
| `lineWidth`    | number       | `2`                           | Độ dày nét vẽ                                       |

Example:

```html
<hs-paint style="height: 200px;"
  [lineColor]="'#00F'"
  [lineWidth]="4"
  defaultValue="assets/img/TaiMuiHong.png"
  [value]="context.tempData.hsThongTinBenhAn.NoiDungChiTietObj.ImgTaiMuiHong"
  update="tempData.hsThongTinBenhAn.NoiDungChiTietObj.ImgTaiMuiHong">
</hs-paint>
