# 3.4.6. Kiểm thử chức năng Nạp tiền

---

## Kiểm thử hàm `validateInputNapTien()`

**Dữ liệu truyền vào:**

```
target = NguoiDung { soTaiKhoan = "123456", vaiTro = "nguoi_dung", trangThai = "hoat_dong" }
admin  = "admin"
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `target = null`, `soTienStr = "50000"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Vui lòng nhập STK hợp lệ trước khi nạp tiền!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC06 | `target = NguoiDung { soTaiKhoan = "123456", vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `soTienStr = "50000"`, `soTaiKhoanAdmin = null` | Gọi hàm validateInputNapTien() | `"Không xác định được tài khoản Admin để ghi lịch sử giao dịch!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC07 | `target = NguoiDung { soTaiKhoan = "123456", vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `soTienStr = "50000"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `target = null`, `soTienStr = "50000"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Vui lòng nhập STK hợp lệ trước khi nạp tiền!"` | Pass |
| TC02 | `target = target`, `soTienStr = " "`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Vui lòng nhập số tiền cần nạp!"` | Pass |
| TC03 | `target = target`, `soTienStr = "..."`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Số tiền không hợp lệ!"` | Pass |
| TC04 | `target = target`, `soTienStr = "0"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Số tiền nạp phải lớn hơn 0!"` | Pass |
| TC05 | `target = target`, `soTienStr = "1000000000000"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `"Số tiền nạp quá lớn!"` | Pass |
| TC06 | `target = target`, `soTienStr = "50000"`, `soTaiKhoanAdmin = null` | Gọi hàm validateInputNapTien() | `"Không xác định được tài khoản Admin để ghi lịch sử giao dịch!"` | Pass |
| TC07 | `target = target`, `soTienStr = "50000"`, `soTaiKhoanAdmin = "admin"` | Gọi hàm validateInputNapTien() | `null` (hợp lệ) | Pass |
