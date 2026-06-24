# 3.4.7. Kiểm thử chức năng Quản lý danh mục thu, chi (Admin)

---

## Kiểm thử hàm `validateInputDanhMuc()`

> Hàm được kiểm thử trên cả 2 controller: `AdminIncomeCategoryController` (thu) và `AdminExpenseCategoryController` (chi)

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `tenDanhMuc = ""`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `"Vui lòng nhập tên danh mục!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC02 | `tenDanhMuc = "Lương"`, `daTrung = true` | Gọi hàm validateInputDanhMuc() | `"Tên danh mục đã tồn tại! Vui lòng nhập tên khác."` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC03 | `tenDanhMuc = "Lương"`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC01 | `tenDanhMuc = ""`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `"Vui lòng nhập tên danh mục!"` | Pass |
| TC02 | `tenDanhMuc = "Lương"`, `daTrung = true` | Gọi hàm validateInputDanhMuc() | `"Tên danh mục đã tồn tại! Vui lòng nhập tên khác."` | Pass |
| TC03 | `tenDanhMuc = "Lương"`, `daTrung = false` | Gọi hàm validateInputDanhMuc() | `null` (hợp lệ) | Pass |

---

## Kiểm thử hàm `validateInputChonDanhMuc()`

**Dữ liệu truyền vào:**

```
dmThu = new DanhMuc(1, "Lương",    "Danh mục thu nhập",  "thu", null)
dmChi = new DanhMuc(2, "Ăn uống", "Danh mục chi tiêu",  "chi", null)
```

---

### Kết quả thực thi kịch bản 1

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC04 | `selected = null`, `hanhDong = "xoa"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục cần xóa!"` | Pass |

---

### Kết quả thực thi kịch bản 2

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC05 | `selected = null`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục cần sửa!"` | Pass |

---

### Kết quả thực thi kịch bản 3

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC06 | `selected = dmThu` (hoặc `dmChi`), `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `null` (hợp lệ, không có lỗi) | Pass |

---

### Các testcase còn lại

| Testcase | Inputs | Steps | Expected Result | Status |
|---|---|---|---|---|
| TC04 | `selected = null`, `hanhDong = "xoa"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục cần xóa!"` | Pass |
| TC05 | `selected = null`, `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `"Vui lòng chọn danh mục cần sửa!"` | Pass |
| TC06 | `selected = dmThu` (hoặc `dmChi`), `hanhDong = "sua"` | Gọi hàm validateInputChonDanhMuc() | `null` (hợp lệ) | Pass |
