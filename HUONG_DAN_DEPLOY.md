# 🚀 Hướng dẫn Deploy Hugo Site lên GitHub Pages

## 📋 Tổng quan

Có 2 cách chính để deploy Hugo site lên GitHub Pages:
1. **Deploy thủ công** - Push thư mục `public/` lên branch `gh-pages`
2. **Deploy tự động** - Sử dụng GitHub Actions (khuyến nghị)

## 🔧 Cách 1: Deploy thủ công (Đơn giản)

### Bước 1: Khởi tạo Git repository

```bash
cd /Users/vanduc/Documents/study/AWS/fcj-workshop-template-main
git init
```

### Bước 2: Tạo file .gitignore

Tạo file `.gitignore` với nội dung:

```
# Hugo
public/
resources/
.hugo_build.lock

# OS
.DS_Store
Thumbs.db

# Editor
.vscode/
.idea/
*.swp
*.swo
```

### Bước 3: Build site

```bash
hugo --minify
```

### Bước 4: Thêm và commit code

```bash
git add .
git commit -m "Initial commit"
```

### Bước 5: Tạo repository trên GitHub

1. Đăng nhập GitHub
2. Tạo repository mới (ví dụ: `workshop-template`)
3. **KHÔNG** tích "Initialize with README"

### Bước 6: Push code lên GitHub

```bash
git remote add origin https://github.com/YOUR_USERNAME/workshop-template.git
git branch -M main
git push -u origin main
```

### Bước 7: Deploy thư mục public lên gh-pages

```bash
# Vào thư mục public
cd public

# Khởi tạo git trong public
git init
git add .
git commit -m "Deploy site"

# Tạo branch gh-pages và push
git branch -M gh-pages
git remote add origin https://github.com/YOUR_USERNAME/workshop-template.git
git push -u origin gh-pages
```

### Bước 8: Cấu hình GitHub Pages

1. Vào repository trên GitHub
2. Settings → Pages
3. Source: chọn branch `gh-pages` và folder `/ (root)`
4. Save

**URL site:** `https://YOUR_USERNAME.github.io/workshop-template/`

---

## 🤖 Cách 2: Deploy tự động với GitHub Actions (Khuyến nghị)

### Bước 1-6: Giống như Cách 1

### Bước 7: Tạo GitHub Actions workflow

Tạo file `.github/workflows/gh-pages.yml`:

```yaml
name: Deploy Hugo site to Pages

on:
  push:
    branches:
      - main  # hoặc master

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  runs-on: ubuntu-latest

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: 'latest'
          extended: true

      - name: Build
        run: hugo --minify

      - name: Setup Pages
        uses: actions/configure-pages@v4

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

### Bước 8: Push code lên GitHub

```bash
git add .
git commit -m "Add GitHub Actions workflow"
git push origin main
```

### Bước 9: Cấu hình GitHub Pages

1. Vào repository → Settings → Pages
2. Source: chọn "GitHub Actions"
3. Save

GitHub Actions sẽ tự động build và deploy mỗi khi bạn push code lên branch `main`.

---

## ⚙️ Cấu hình quan trọng

### 1. Cập nhật baseURL trong config.toml

Mở file `config.toml` và sửa `baseURL`:

```toml
baseURL = "https://YOUR_USERNAME.github.io/workshop-template/"
```

**Lưu ý:** 
- Thay `YOUR_USERNAME` bằng username GitHub của bạn
- Thay `workshop-template` bằng tên repository của bạn
- URL phải kết thúc bằng `/`

### 2. Kiểm tra file .gitignore

Đảm bảo file `.gitignore` có:
```
public/
resources/
.hugo_build.lock
```

---

## 📝 Checklist trước khi deploy

- [ ] Đã build site thành công: `hugo --minify`
- [ ] Đã cập nhật `baseURL` trong `config.toml`
- [ ] Đã tạo file `.gitignore`
- [ ] Đã kiểm tra tất cả các file đã được commit
- [ ] Đã tạo repository trên GitHub
- [ ] Đã push code lên GitHub
- [ ] Đã cấu hình GitHub Pages

---

## 🔄 Cập nhật site sau khi thay đổi

### Nếu dùng Cách 1 (thủ công):

```bash
# 1. Sửa code trong content/
# 2. Build lại
hugo --minify

# 3. Vào thư mục public và push
cd public
git add .
git commit -m "Update content"
git push origin gh-pages
```

### Nếu dùng Cách 2 (GitHub Actions):

```bash
# 1. Sửa code trong content/
# 2. Commit và push
git add .
git commit -m "Update content"
git push origin main

# GitHub Actions sẽ tự động build và deploy
```

---

## 🐛 Xử lý lỗi thường gặp

### Lỗi 404 - Page not found

- Kiểm tra `baseURL` trong `config.toml` có đúng không
- Đảm bảo URL kết thúc bằng `/`
- Xóa cache trình duyệt

### Site không cập nhật

- Kiểm tra GitHub Actions có chạy thành công không
- Đợi vài phút để GitHub xử lý
- Xóa cache trình duyệt (Ctrl+Shift+R)

### Lỗi build

- Kiểm tra Hugo version: `hugo version`
- Kiểm tra lỗi trong GitHub Actions logs
- Test build local: `hugo --minify`

---

## 📚 Tài liệu tham khảo

- [Hugo Documentation](https://gohugo.io/documentation/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions for Hugo](https://github.com/peaceiris/actions-hugo)

