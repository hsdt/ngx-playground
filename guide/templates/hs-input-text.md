# hs-input-text

`<hs-input-text>` là một component input nhập liệu trên 1 dòng.

| Thuộc tính   | Kiểu dữ liệu | Mặc định | Mô tả                                               |
|--------------|--------------|----------|-----------------------------------------------------|
| `value`      | string       | -        | Giá trị hiện tại của input                          |
| `update`     | string       | -        | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `label`      | string       | `''`     | Nhãn hiển thị phía trên input                       |
| `inputId`    | string       | -        | ID duy nhất cho phần tử input                       |
| `disabled`   | boolean      | `false`  | Vô hiệu hóa input                                   |
| `labelStyle` | string       | `''`     | Inline style cho nhãn                               |
| `inputStyle` | string       | `''`     | Inline style cho input                              |
| `maxlength`  | number       | `2000`   | Số ký tự tối đa                                     |
| `type`       | string       | `'text'` | Loại input (`text`, `number`,...)                   |
| `style`      | string       | `''`     | Inline style cho element                            |
| `class`      | string       | `''`     | Class CSS cho element                               |

Example:

```html
<hs-input-text
  label="Họ tên bệnh nhân:"
  [value]="context.TenBenhNhan"
  update="TenBenhNhan"
  labelStyle="color: red;"
  inputStyle="font-weight: bold;"
  maxlength="100">
</hs-input-text>
