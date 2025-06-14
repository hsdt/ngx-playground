# hs-input-wrapper

`<hs-input-wrapper>` là một component dùng để bao bọc thẻ `<input>` (hoặc `<input type="checkbox">`), Component này hoạt động như một bridge giữa input HTML và cơ chế binding Angular.

| Thuộc tính | Kiểu dữ liệu | Mặc định | Mô tả                                               |
|------------|--------------|----------|-----------------------------------------------------|
| `value`    | string       | `''`     | Giá trị được truyền vào cho thẻ input con           |
| `update`   | string       | `''`     | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `style`    | string       | `''`     | Inline style cho element                            |
| `class`    | string       | `''`     | Class CSS cho element                               |

> 📌 Lưu ý: Component chỉ hoạt động với 1 phần tử `<input>` duy nhất được bao bọc trong hs-input-wrapper.

Example

```html
<hs-input-wrapper [value]="context.email" update="email">
  <input type="text" />
</hs-input-wrapper>

<hs-input-wrapper [value]="context.isActive" update="isActive">
  <input type="checkbox" />
</hs-input-wrapper>
