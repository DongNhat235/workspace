# Hướng dẫn triển khai (GitHub Pages)

Hai cách phổ biến để deploy site tĩnh này lên GitHub Pages:

## 1) GitHub Pages (user/organization site)
- Nếu muốn trang của bạn chạy ở `https://username.github.io`, tạo repo tên `username.github.io` và push nội dung vào branch `main`.
- Vào **Settings → Pages** và chọn branch `main` để serve (thư mục `/(root)`).

## 2) GitHub Pages (project site) bằng gh-pages branch
- Bạn có thể deploy vào branch `gh-pages` và bật Pages từ `gh-pages`.
- Có thể dùng action hoặc `git subtree` để push `gh-pages`.

## Tạo repo từ CLI (yêu cầu `gh`):
```bash
gh repo create username/my-portfolio --public --source=. --remote=origin --push
```

## Gợi ý: tự động deploy với Action
- Tạo `GITHUB_TOKEN` (action mặc định đã có), dùng `peaceiris/actions-gh-pages` nếu muốn deploy build pipeline.

