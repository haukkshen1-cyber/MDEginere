# 3.4.5. Kiểm thử chức năng Quản lý tài khoản

---

## Kiểm thử hàm `validateInputKhoaTaiKhoan()`

**Dữ liệu truyền vào:**

```
quan_ly_hoat_dong  = NguoiDung { vaiTro = "quan_ly",   trangThai = "hoat_dong" }
nguoi_dung_bi_khoa = NguoiDung { vaiTro = "nguoi_dung", trangThai = "bi_khoa"   }
nguoi_dung_hoat_dong = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `selected = null` | Gọi hàm validateInputKhoaTaiKhoan() | `"Vui lòng chọn tài khoản cần khóa!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC02 | `selected = NguoiDung { vaiTro = "quan_ly", trangThai = "hoat_dong" }` | Gọi hàm validateInputKhoaTaiKhoan() | `"Không thể khóa tài khoản Admin!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC04 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputKhoaTaiKhoan() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `selected = null` | Gọi hàm validateInputKhoaTaiKhoan() | `"Vui lòng chọn tài khoản cần khóa!"` | Pass |
| TC02 | `selected = NguoiDung { vaiTro = "quan_ly", trangThai = "hoat_dong" }` | Gọi hàm validateInputKhoaTaiKhoan() | `"Không thể khóa tài khoản Admin!"` | Pass |
| TC03 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "bi_khoa" }` | Gọi hàm validateInputKhoaTaiKhoan() | `"Tài khoản này đã bị khóa!"` | Pass |
| TC04 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputKhoaTaiKhoan() | `null` (hợp lệ) | Pass |

---

## Kiểm thử hàm `validateInputMoKhoaTaiKhoan()`

**Dữ liệu truyền vào:**

```
nguoi_dung_hoat_dong = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }
nguoi_dung_bi_khoa   = NguoiDung { vaiTro = "nguoi_dung", trangThai = "bi_khoa"   }
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC05 | `selected = null` | Gọi hàm validateInputMoKhoaTaiKhoan() | `"Vui lòng chọn tài khoản cần mở khóa!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC06 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputMoKhoaTaiKhoan() | `"Tài khoản này đang hoạt động bình thường!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC07 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "bi_khoa" }` | Gọi hàm validateInputMoKhoaTaiKhoan() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC05 | `selected = null` | Gọi hàm validateInputMoKhoaTaiKhoan() | `"Vui lòng chọn tài khoản cần mở khóa!"` | Pass |
| TC06 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputMoKhoaTaiKhoan() | `"Tài khoản này đang hoạt động bình thường!"` | Pass |
| TC07 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "bi_khoa" }` | Gọi hàm validateInputMoKhoaTaiKhoan() | `null` (hợp lệ) | Pass |

---

## Kiểm thử hàm `validateInputXemThongTinTaiKhoan()`

**Dữ liệu truyền vào:**

```
selected  = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }
thongTin  = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC08 | `selected = null`, `thongTinNguoiDung = null` | Gọi hàm validateInputXemThongTinTaiKhoan() | `"Vui lòng chọn user cần xem thông tin!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC09 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `thongTinNguoiDung = null` | Gọi hàm validateInputXemThongTinTaiKhoan() | `"Không tìm thấy thông tin người dùng trong cơ sở dữ liệu!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC10 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `thongTinNguoiDung = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputXemThongTinTaiKhoan() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC08 | `selected = null`, `thongTinNguoiDung = null` | Gọi hàm validateInputXemThongTinTaiKhoan() | `"Vui lòng chọn user cần xem thông tin!"` | Pass |
| TC09 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `thongTinNguoiDung = null` | Gọi hàm validateInputXemThongTinTaiKhoan() | `"Không tìm thấy thông tin người dùng trong cơ sở dữ liệu!"` | Pass |
| TC10 | `selected = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }`, `thongTinNguoiDung = NguoiDung { vaiTro = "nguoi_dung", trangThai = "hoat_dong" }` | Gọi hàm validateInputXemThongTinTaiKhoan() | `null` (hợp lệ) | Pass |
ripcord-camera


Commit & Push

Changes
Repo Files
Checks


Compare against:

origin/main



Setup
Run
