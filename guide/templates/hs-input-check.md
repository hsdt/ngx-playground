# hs-input-check

`<hs-input-check>` là một component checkbox đa năng với nhiều tùy chọn hiển thị.

| Thuộc tính          | Kiểu              | Mặc định | Mô tả                                                                           |
|---------------------|-------------------|----------|---------------------------------------------------------------------------------|
| `selectedValue`     | string \| boolean | -        | Giá trị được chọn                                                               |
| `update`            | string            | -        | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi                             |
| `value`             | any               | -        | Giá trị của checkbox                                                            |
| `inputId`           | string            | Auto-gen | ID duy nhất cho input                                                           |
| `inputName`         | string            | -        | Thuộc tính name của input                                                       |
| `disabled`          | boolean           | false    | Vô hiệu hóa checkbox                                                            |
| `readonly`          | boolean           | false    | Chế độ chỉ đọc                                                                  |
| `beforeText`        | string            | -        | Text hiển thị trước checkbox                                                    |
| `afterText`         | string            | -        | Text hiển thị sau checkbox                                                      |
| `size`              | string            | 'lg'     | Kích thước (sm, md, lg, xl)                                                     |
| `clearOnUnCheckIds` | string[]          | []       | Danh sách ID các phần tử sẽ reset khi uncheck                                   |
| `confirmEnabled`    | boolean           | false    | Yêu cầu xác nhận clear input có id được khai truyền vào trong clearOnUnCheckIds |

Example:

```html
<hs-input-check
  [selectedValue]="context.tempData.hsBenhAn.BenhNhan.GioiTinh"
  update="tempData.hsBenhAn.BenhNhan.GioiTinh"
  [value]="true"
  afterText="1. Nam">
</hs-input-check>
<hs-input-check
  [selectedValue]="context.tempData.hsBenhAn.BenhNhan.GioiTinh"
  update="tempData.hsBenhAn.BenhNhan.GioiTinh"
  [value]="false"
  afterText="2. Nữ">
</hs-input-check>
