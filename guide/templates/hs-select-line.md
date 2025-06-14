# hs-select-line

`<hs-select-line>` là một component dạng dropdown có hỗ trợ tìm kiếm, chọn một hoặc nhiều giá trị.

| Thuộc tính     | Kiểu dữ liệu      | Mặc định      | Mô tả                                               |
|----------------|-------------------|---------------|-----------------------------------------------------|
| `value`        | string / string[] | `''`          | Giá trị hiện tại của dropdown                       |
| `update`       | string            | `''`          | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `label`        | string            | `''`          | Nhãn hiển thị phía trước select                     |
| `labelStyle`   | string            | `''`          | Inline style cho nhãn (`label`)                     |
| `bindLabel`    | string            | `''`          | Tên thuộc tính của object hiển thị trong dropdown   |
| `bindValue`    | string            | `''`          | Tên thuộc tính của object dùng làm giá trị          |
| `placeholder`  | string            | `''`          | Placeholder hiển thị khi không có giá trị           |
| `multiple`     | boolean           | `false`       | Cho phép chọn nhiều giá trị nếu là `true`           |
| `disabled`     | boolean           | `false`       | Vô hiệu hóa dropdown nếu là `true`                  |
| `readonly`     | boolean           | `false`       | Chỉ đọc, không cho phép thay đổi nếu là `true`      |
| `items`        | any[]             | `[]`          | Danh sách dữ liệu để hiển thị trong dropdown        |
| `searchByKeys` | string[]          | `[bindLabel]` | Các thuộc tính dùng để tìm kiếm                     |
| `style`        | string            | `''`          | Inline style cho component                          |
| `class`        | string            | `''`          | Class CSS cho component                             |

Example:

```html
<hs-select-line
  [items]="context.tempData.dmTinhThanh"
  [value]="context.tempData.hsBenhAn.BenhNhan.IdTinhThanh"
  update="tempData.hsBenhAn.BenhNhan.IdTinhThanh"
  bindLabel="Ten" bindValue="Id"
  [searchByKeys]="['Ma', 'Ten']"
></hs-select-line>
