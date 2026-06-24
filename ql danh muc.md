# 3.4.3. Kiểm thử chức năng Quản lý danh mục (User)

---

## Kiểm thử hàm `validateInputDanhMuc()`

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `tenDanhMuc = ""`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `"Vui lòng nhập tên danh mục!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC02 | `tenDanhMuc = "Ăn uống"`, `daTrung = true` | Gọi hàm validateInputDanhMuc() | `"Tên danh mục đã tồn tại! Vui lòng nhập tên khác."` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC03 | `tenDanhMuc = "Ăn uống"`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `tenDanhMuc = ""`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `"Vui lòng nhập tên danh mục!"` | Pass |
| TC02 | `tenDanhMuc = "Ăn uống"`, `daTrung = true` | Gọi hàm validateInputDanhMuc() | `"Tên danh mục đã tồn tại! Vui lòng nhập tên khác."` | Pass |
| TC03 | `tenDanhMuc = "Ăn uống"`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `null` (hợp lệ) | Pass |

---

## Kiểm thử hàm `validateInputChonDanhMuc()`

**Dữ liệu truyền vào:**

```
dmMacDinh = new DanhMuc(1, "An uong", "Danh muc mac dinh", "chi", null)
dmThuong  = new DanhMuc(2, "An uong", "Danh muc cua user", "chi", "123")
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC08 | `selected = null`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC09 | `selected = dmMacDinh`, `hanhDong = "xoa"` | Gọi hàm validateInputChonDanhMuc() | `"Không thể xóa danh mục mặc định!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC10 | `selected = dmMacDinh`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Không thể sửa danh mục mặc định!"` | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC08 | `selected = null`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục!"` | Pass |
| TC09 | `selected = dmMacDinh`, `hanhDong = "xoa"` | Gọi hàm validateInputChonDanhMuc() | `"Không thể xóa danh mục mặc định!"` | Pass |
| TC10 | `selected = dmMacDinh`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Không thể sửa danh mục mặc định!"` | Pass |
| TC11 | `selected = dmThuong`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `null` (hợp lệ) | Pass |
