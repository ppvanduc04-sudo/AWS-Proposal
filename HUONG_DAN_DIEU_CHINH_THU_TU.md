# 📋 Hướng dẫn tự điều chỉnh thứ tự các section

## 🎯 Cách điều chỉnh thứ tự

### Bước 1: Mở file cần chỉnh

Mỗi section có 1 file `_index.vi.md` trong thư mục của nó:

```
content/
├── 1-Worklog/
│   └── _index.vi.md          ← Chỉnh file này
├── 2-Proposal/
│   └── _index.vi.md          ← Chỉnh file này
├── 3-BlogsTranslated/
│   └── _index.vi.md          ← Chỉnh file này
├── 4-EventParticipated/
│   └── _index.vi.md          ← Chỉnh file này
├── 5-Workshop/
│   └── _index.vi.md          ← Chỉnh file này
├── 6-Self-evaluation/
│   └── _index.vi.md          ← Chỉnh file này
└── 7-Feedback/
    └── _index.vi.md          ← Chỉnh file này
```

### Bước 2: Tìm và chỉnh số `weight`

Mở file `_index.vi.md` và tìm phần **front matter** ở đầu file:

```yaml
---
title: "Tên section"
date: "2025-10-01"
weight: 2              ← CHỈNH SỐ NÀY
chapter: false
pre: " <b> 2. </b> "
---
```

### Bước 3: Đổi số `weight`

**Quy tắc:**
- Số **nhỏ hơn** = hiển thị **trước** (trên)
- Số **lớn hơn** = hiển thị **sau** (dưới)
- Số **1** = đứng đầu tiên

**Ví dụ:**

Nếu muốn **Workshop (5)** đứng trước **Proposal (2)**:

1. Mở `content/5-Workshop/_index.vi.md`
2. Đổi `weight: 5` thành `weight: 1`
3. Mở `content/2-Proposal/_index.vi.md`
4. Đổi `weight: 2` thành `weight: 3`

Kết quả: Workshop sẽ đứng trước Proposal.

## 📊 Thứ tự hiện tại

| Thứ tự | Section | File cần chỉnh | Weight hiện tại |
|--------|---------|----------------|----------------|
| 1 | Worklog | `content/1-Worklog/_index.vi.md` | 1 |
| 2 | Proposal | `content/2-Proposal/_index.vi.md` | 2 |
| 3 | BlogsTranslated | `content/3-BlogsTranslated/_index.vi.md` | 3 |
| 4 | EventParticipated | `content/4-EventParticipated/_index.vi.md` | 4 |
| 5 | Workshop | `content/5-Workshop/_index.vi.md` | 5 |
| 6 | Self-evaluation | `content/6-Self-evaluation/_index.vi.md` | 6 |
| 7 | Feedback | `content/7-Feedback/_index.vi.md` | 7 |

## ⚠️ Lưu ý quan trọng

1. **Không được có 2 section cùng weight** - sẽ gây lỗi sắp xếp
2. **Chỉ chỉnh số `weight`** - không cần chỉnh các dòng khác
3. **Sau khi chỉnh**, chạy lại Hugo để xem kết quả:
   ```bash
   hugo server
   ```

## 🔍 Kiểm tra thứ tự sau khi chỉnh

Chạy lệnh này để xem thứ tự hiện tại:

```bash
for dir in content/*/; do 
  if [ -f "${dir}_index.vi.md" ]; then 
    weight=$(grep '^weight:' "${dir}_index.vi.md" | cut -d: -f2 | tr -d ' ')
    echo "$weight. $(basename "$dir")"
  fi
done | sort -n
```

## 💡 Ví dụ thực tế

**Ví dụ 1:** Muốn Workshop đứng thứ 2 (sau Worklog)

1. Mở `content/5-Workshop/_index.vi.md`
2. Đổi `weight: 5` → `weight: 2`
3. Mở `content/2-Proposal/_index.vi.md`
4. Đổi `weight: 2` → `weight: 3`
5. Mở `content/3-BlogsTranslated/_index.vi.md`
6. Đổi `weight: 3` → `weight: 4`
7. ... (tăng tất cả các weight phía sau lên 1)

**Ví dụ 2:** Muốn đổi chỗ 2 section

Giả sử muốn đổi chỗ Proposal (2) và BlogsTranslated (3):

1. `content/2-Proposal/_index.vi.md`: `weight: 2` → `weight: 3`
2. `content/3-BlogsTranslated/_index.vi.md`: `weight: 3` → `weight: 2`

Xong! Đơn giản vậy thôi.

