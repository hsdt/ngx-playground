# hs-textarea-line

`<hs-textarea-line>` là một component input nhập liệu trên nhiều dòng.

| Thuộc tính      | Kiểu dữ liệu | Mặc định | Mô tả                                             |
|-----------------|--------------|----------|---------------------------------------------------|
| `value`         | string       | -        | Giá trị hiện tại của textarea                     |
| `update`        | string       | -        | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `label`         | string       | `''`     | Nhãn hiển thị phía trên textarea                  |
| `textareaId`    | string       | -        | ID duy nhất cho phần tử textarea                  |
| `disabled`      | boolean      | `false`  | Vô hiệu hóa textarea                              |
| `maxlength`     | number       | `2000`   | Số ký tự tối đa                                   |
| `labelStyle`    | string       | `''`     | Inline style cho nhãn                             |
| `textareaStyle` | string       | `''`     | Inline style cho textarea                         |
| `style`         | string       | `''`     | Inline style cho element                      |
| `class`         | string       | `''`     | Class CSS cho element                         |

Example:

```html
<hs-textarea-line
  label="Họ tên bệnh nhân:"
  [value]="context.TenBenhNhan"
  update="TenBenhNhan"
  labelStyle="color: red;"
  textareaStyle="font-weight: bold;"
  maxlength="100">
</hs-textarea-line>
