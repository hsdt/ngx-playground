# hs-signature

Tạo vị trí ký trên mẫu phiếu, chức năng:
- Vị trí ký điện tử
- Vị trí ký số

Example:

```
<hs-signature
  signaturePositionCode="BacSi"
  [signatureHistory]="context.tempData.DSHSLichSuKySos['BacSi']">
</hs-signature>
```

Trong đó:
* signaturePositionCode: Mã vị trí ký
* signatureHistory: Lịch sử vị trí ký `BacSi`
