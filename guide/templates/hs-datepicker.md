# hs-datepicker

| Thuộc tính    | Kiểu          | Mặc định     | Mô tả                   |
|---------------|---------------|--------------|-------------------------|
| `value`       | dateISOString | ''           | Giá trị ngày            |
| `update`      | string        | ''           | Tên trường dữ liệu      |
| `label`       | string        | ''           | Nhãn hiển thị           |
| `format`      | string        | 'dd/MM/yyyy' | Định dạng hiển thị ngày |
| `placeholder` | string        | ''           | Placeholder text        |
| `disabled`    | boolean       | false        | Vô hiệu hóa component   |
| `readonly`    | boolean       | false        | Chế độ chỉ đọc          |

Example:

```html
<!-- Cách sử dụng cơ bản với định dạng mặc định -->
<hs-datepicker
  [value]="context.ThoiGian"
  update="ThoiGian"
  label="Ngày tái khám:">
</hs-datepicker>

<!-- Với định dạng tùy chỉnh format="dd/MM/yyyy HH:mm"-->
<!-- 15/07/2023 14:30 -->
<hs-datepicker
  [value]="context.ThoiGian"
  update="ThoiGian"
  label="Giờ hẹn:"
  format="dd/MM/yyyy HH:mm"
</hs-datepicker>
