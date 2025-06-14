# hs-input-otp

`<hs-input-otp>` là một component dùng để nhập mã OTP hoặc chuỗi nhiều phần theo độ dài định sẵn. Mỗi khối input hiển thị tương ứng với một phần ký tự trong chuỗi đầu vào.

| Thuộc tính   | Kiểu dữ liệu | Mặc định  | Mô tả                                                               |
|--------------|--------------|-----------|---------------------------------------------------------------------|
| `value`      | string       | `''`      | Giá trị hiện tại của OTP/mã xác thực                                |
| `update`     | string       | `''`      | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi                 |
| `length`     | number       | -         | Số lượng khối (block) nhập ký tự, mặc định theo `maskLength.length` |
| `maskLength` | number[]     | `[1,...]` | Độ dài ký tự cho từng khối, nếu không khai báo mặc định là 1        |
| `readonly`   | boolean      | `false`   | Chỉ đọc, không cho nhập dữ liệu nếu là `true`                       |
| `disabled`   | boolean      | `false`   | Vô hiệu hóa component nếu là `true`                                 |
| `style`      | string       | `''`      | Inline style cho element                                            |
| `class`      | string       | `''`      | Class CSS cho element                                               |

Example:

```html
<hs-input-otp
  [value]="context.SoBHYT"
  update="SoBHYT"
  [length]="4"
  [maskLength]="[2,1,2,2,3,5]">
</hs-input-otp>
