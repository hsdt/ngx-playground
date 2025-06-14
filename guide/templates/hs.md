# hs

Component `<hs>` là một thành phần hiển thị văn bản, hỗ trợ pipe tùy biến và hoạt động linh hoạt.

- Hỗ trợ pipe tùy chỉnh (`date`, `uppercase`, `exp`, ...)
- Gán class tự động theo thẻ HTML (`h1`, `div`, `span`, ...)
- Tự động cập nhật nội dung khi dùng pipe `"exp"` (expression binding)

| Thuộc tính | Kiểu dữ liệu | Mặc định | Mô tả                                                               |
|------------|--------------|----------|---------------------------------------------------------------------|
| `if`       | `boolean`    | `true`   | Kiểm soát điều kiện hiển thị nội dung                               |
| `text`     | `string`     | `''`     | Nội dung văn bản để hiển thị (có thể dùng pipe)                     |
| `pipeName` | `string`     | `''`     | Tên của pipe áp dụng cho `text` (ví dụ: `date`, `uppercase`, `exp`) |
| `pipeArgs` | `any[]`      | `[]`     | Tham số truyền vào pipe                                             |
| `tag`      | `string`     | `'div'`  | Tên thẻ HTML để ánh xạ thành class tương ứng                        |
| `style`    | `string`     | `''`     | Inline style cho element                                            |
| `class`    | `string`     | `''`     | Class CSS cho element                                               |

Class ánh xạ theo thẻ

Tùy theo giá trị của `tag`, component tự động gán class tương ứng:

| tag/class hỗ trợ | Ý nghĩa            |
|------------------|--------------------|
| `div`            | Thẻ block cơ bản   |
| `h1` → `h6`      | Tiêu đề cấp độ 1–6 |
| `span`           | Nội dung inline    |
| `b`              | Chữ đậm            |
| `i`              | Chữ nghiêng        |
| `small`          | Cỡ chữ nhỏ         |
| `pre`            | Preserve format    |

Example:

```html

<hs text="Tiêu đề" tag="h2" class="text-primary"></hs>
<hs [text]="context.TieuDe" tag="h2" class="text-primary"></hs>

<!-- Với pipeName="date" và [pipeArgs]="['dd/MM/yyyy']" -->
<hs
  text="2004-01-19T00:00:00"
  pipeName="date"
  [pipeArgs]="['dd/MM/yyyy']"
  tag="small">
</hs>
<!-- output = 19/01/2004 -->

