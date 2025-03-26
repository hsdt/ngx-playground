# Mẫu ví dụ đơn giản nhất

Ví dụ sau đây tạo ra một mẫu phiếu ` Bìa bệnh án`, trong đó người hỗ trợ có thể tùy chỉnh tùy ý về tên, kích thước văn bản hiển thị, các ô tích xuất hiện trên mẫu phiếu.

Việc này cho phép cán bộ hỗ trợ người dùng có thể thay đổi những yêu cầu đơn giản của người dùng mà không cần phải can thiệp sâu vào hệ thống.

Ví dụ:

```html
<div class="page-content page-a4 font-times-new-roman">
  <div style="line-height: 25px; font-family: 'Times New Roman', Times, serif; height: 1024px; overflow: hidden; border: 3px solid;">
    <div style="height: 69px; border-bottom: 1px solid #000000; padding-top: 10px; line-height: 30px;">
      <div style="width: 100%; float: left; font-size: 24px;" align="center">
        <div><strong><hs tag="span" [text]="context.BenhAnChiTiet.CoSoTrucThuoc"></hs></strong></div>
        <div><strong><hs tag="span" [text]="context.BenhAnChiTiet.TenBenhVien"></hs></strong></div>
      </div>
    </div>
    <div style="text-align: center; font-size: 40px; margin-top: 80px; font-weight: bold; line-height: 68px;">
      BỆNH ÁN <hs tag="span" [text]="context.loaiBenhAn.Ten"></hs>
    </div>
    <div style="text-align: center; font-size: 30px; font-weight: bold; line-height: 36px;">
    </div>
    <div
      style="text-align: center; font-size: 30px; font-weight: bold; line-height: 36px;">
        Khoa <hs tag="span" [text]="context.hsBenhAn.TenKhoaKham"></hs>
    </div>
    <br />
    <div style="text-align: center; font-size: 22px; font-weight: bold; margin: 10px;">
      NĂM: <hs tag="span" [text]="context.hsBenhAn.NgayVaoVien" pipeName="date"></hs>
    </div>
    <br />
    <div style="width: 100%; margin-top: 100px; font-size: 20px; line-height: 30px; height: 160px;">
      <div style="width: 100%; padding-left: 20px; overflow: hidden;">
        <div style="float: left; width: 60%;">
          HỌ VÀ TÊN: <strong style="text-transform: uppercase;"><hs tag="span" [text]="context.hsBenhAn.BenhNhan.HoTen"></hs></strong>
        </div>
        <div style="float: left; width: 40%;">
          <hs-input-check size="xl" name="gender" [selectedValue]="context.hsBenhAn.BenhNhan.GioiTinh" update="hsBenhAn.BenhNhan.GioiTinh" [value]="true" beforeText="Nam"></hs-input-check>
          <hs-input-check size="xl" name="gender" [selectedValue]="context.hsBenhAn.BenhNhan.GioiTinh" update="hsBenhAn.BenhNhan.GioiTinh" [value]="false" beforeText="Nữ"></hs-input-check>
        </div>
      </div>
      <div style="width: 100%; padding-left: 20px; overflow: hidden;">
        <div style="float: left; width: 50%;">Năm sinh: <hs tag="span" [text]="context.hsBenhAn.BenhNhan.NgaySinh"></hs></div>
        <div style="float: left; width: 50%;">Dân tộc: <hs tag="span" [text]="context.hsBenhAn.BenhNhan.TenDanToc"></hs></div>
      </div>
      <div style="width: 100%; padding-left: 20px;">
        <div>Địa chỉ: <hs tag="span" [text]="context.hsBenhAn.BenhNhan.DiaChi"></hs></div>
      </div>
      <div style="width: 100%; padding-left: 20px; overflow: hidden;">
        <div style="float: left; width: 50%;">
          Số điện thoại: &nbsp;&nbsp;<hs [text]="context.hsBenhAn.BenhNhan.DienThoai" tag="span"></hs>
        </div>
      </div>
    </div>
    <div style="width: 80%; margin: 90px auto; border: 1px solid; overflow: hidden;" align="center">
      <div style="float: left; width: 49%; padding: 20px 0;">
        <div><strong>BẮT ĐẦU ĐIỀU TRỊ</strong></div>
        <div>NGÀY: <hs tag="span" [text]="context.hsBenhAn.NgayVaoVien" pipeName="date"></hs></div>
      </div>
      <div style="float: left; width: 50%; border-left: 1px solid; padding: 20px 0;">
        <div><strong>KẾT THÚC ĐIỀU TRỊ</strong></div>
        <div>NGÀY: <hs tag="span" [text]="context.hsBenhAn.NgayRaVien" pipeName="date"></hs></div>
      </div>
    </div>
    <div align="center" style="font-size: 20px;">
      <strong>MÃ BỆNH: &nbsp;&nbsp;<hs tag="span" [text]="context.hsBenhAn.IcdKKBCCMa"></hs>&nbsp;&nbsp;</strong>
    </div>
  </div>
</div>
```
