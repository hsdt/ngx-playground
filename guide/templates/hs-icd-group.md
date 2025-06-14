# hs-icd-group

`<hs-icd-group>` là component chọn mã bệnh ICD (Y học hiện đại/Y học cổ truyền) với hỗ trợ cả chế độ đơn và đa mã bệnh.

| Thuộc tính | Kiểu           | Mặc định | Mô tả                                               |
|------------|----------------|----------|-----------------------------------------------------|
| `icdType`  | 'YHHD'\|'YHCT' | 'YHHD'   | Loại mã bệnh (Y học hiện đại/Y học cổ truyền)       |
| `update`   | string         | ''       | Tên trường dữ liệu sẽ cập nhật khi giá trị thay đổi |
| `multiple` | boolean        | false    | Chế độ nhiều mã bệnh                                |
| `label`    | string         | ''       | Nhãn hiển thị                                       |
| `disabled` | boolean        | false    | Vô hiệu hóa component                               |
| `readonly` | boolean        | false    | Chế độ chỉ đọc                                      |
| `icd`      | any[]          | -        | Danh sách mã bệnh (dùng khi multiple=true)          |
| `icdMa`    | string         | ''       | Mã bệnh (dùng khi multiple=false)                   |
| `icdTen`   | string         | ''       | Tên bệnh (dùng khi multiple=false)                  |

```html
<!-- Chế độ đơn mã bệnh -->
<hs-icd-group label="+ Bệnh chính(tổn thương):"
  [icd]="context.tempData.hsBenhAn.BenhAnChiTietObj.IcdRaVienBenhChinh"
  [icdMa]="context.tempData.hsBenhAn.BenhAnChiTietObj.IcdRaVienBenhChinhMa"
  [icdTen]="context.tempData.hsBenhAn.BenhAnChiTietObj.IcdRaVienBenhChinhTen"
  update="tempData.hsBenhAn.BenhAnChiTietObj.IcdRaVienBenhChinh">
</hs-icd-group>

<!-- Chế độ đa mã bệnh -->
<div>+ Bệnh kèm theo:</div>
<hs-icd-group [icd]="context.tempData.hsBenhAn.BenhAnChiTietObj.ListIcdRaVienBenhKemTheo"
  update="tempData.hsBenhAn.BenhAnChiTietObj.ListIcdRaVienBenhKemTheo" [multiple]="true">
</hs-icd-group>
