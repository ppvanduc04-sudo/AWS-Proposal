# Hướng dẫn sắp xếp vị trí các file và thư mục trong Hugo

## 📋 Tổng quan

Trong Hugo, việc sắp xếp các page và section được điều khiển bởi các tham số trong **front matter** của mỗi file.

## 🔧 Các file cần chỉnh sửa

### 1. **Front Matter của từng file** (QUAN TRỌNG NHẤT)

Mỗi file `_index.vi.md` trong các thư mục tuần cần có các tham số sau:

**Vị trí file:** `content/1-Worklog/1.X-WeekX/_index.vi.md`

```yaml
---
title: "Worklog Tuần X"
date: "2025-XX-XX"    # Ngày bắt đầu tuần (YYYY-MM-DD)
weight: X              # Số thứ tự (1, 2, 3, 4, ...)
chapter: false
pre: " <b> 1.X. </b> "
---
```

**Giải thích:**
- `weight`: Số thứ tự sắp xếp (quan trọng nhất). Hugo sắp xếp theo weight từ nhỏ đến lớn.
- `date`: Ngày bắt đầu tuần. Khi weight bằng nhau, Hugo sẽ sắp xếp theo date.
- `title`: Tiêu đề hiển thị
- `pre`: Tiền tố hiển thị trước title trong menu

**Ví dụ:**
- Tuần 1: `weight: 1`, `date: "2025-09-08"`
- Tuần 2: `weight: 2`, `date: "2025-09-15"`
- Tuần 3: `weight: 3`, `date: "2025-09-22"`
- ...

### 2. **File config.toml** (Tùy chọn)

**Vị trí:** `config.toml` (ở thư mục gốc)

Có thể thêm cấu hình sau vào phần `[params]`:

```toml
[params]
  # Sắp xếp sections theo "weight" (mặc định) hoặc "title"
  ordersectionsby = "weight"  # hoặc "title"
```

**Lưu ý:** Mặc định theme đã sắp xếp theo `weight`, nên không cần thêm cấu hình này trừ khi muốn sắp xếp theo tên.

### 3. **File _index.vi.md của section** (Tùy chọn)

**Vị trí:** `content/1-Worklog/_index.vi.md`

File này là trang index của section Worklog, cũng cần có `weight` để sắp xếp với các section khác:

```yaml
---
title: "Nhật ký công việc"
date: "2025-10-01"
weight: 1              # Thứ tự của section này so với các section khác
chapter: false
pre: " <b> 1. </b> "
---
```

## 📊 Cách Hugo sắp xếp

Hugo sắp xếp theo thứ tự ưu tiên:

1. **Weight** (quan trọng nhất)
   - Số nhỏ hơn = hiển thị trước
   - Nếu weight bằng nhau → chuyển sang bước 2

2. **Date** (khi weight bằng nhau)
   - Ngày cũ hơn = hiển thị trước
   - Nếu date bằng nhau → sắp xếp theo tên file

3. **Tên file** (cuối cùng)
   - Sắp xếp theo thứ tự alphabet

## ✅ Checklist để sắp xếp đúng

- [ ] Tất cả các file `_index.vi.md` có `weight` khác nhau (1, 2, 3, ...)
- [ ] `weight` tăng dần theo thứ tự tuần
- [ ] `date` tăng dần theo thứ tự tuần
- [ ] Không có 2 file có cùng `weight`
- [ ] File `_index.vi.md` của section có `weight` phù hợp

## 🔍 Kiểm tra thứ tự hiện tại

Chạy lệnh sau để kiểm tra weight và date của tất cả các tuần:

```bash
# Kiểm tra weight
for f in content/1-Worklog/1.*-Week*/_index.vi.md; do 
  echo "$(grep '^weight:' "$f" | cut -d: -f2 | tr -d ' '): $(basename $(dirname "$f"))"; 
done | sort -n

# Kiểm tra date
for f in content/1-Worklog/1.*-Week*/_index.vi.md; do 
  echo "$(grep '^date:' "$f" | cut -d: -f2 | tr -d ' \"'): $(basename $(dirname "$f"))"; 
done | sort
```

## 🛠️ Sửa lỗi sắp xếp

Nếu các tuần không hiển thị đúng thứ tự:

1. Kiểm tra `weight` của tất cả các file
2. Đảm bảo `weight` tăng dần từ 1 đến 12
3. Kiểm tra `date` có tăng dần không
4. Xóa cache và rebuild: `rm -rf public resources .hugo_build.lock && hugo`

