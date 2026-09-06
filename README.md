# Bài Tập: Thiết Kế Trang Web Bằng HTML và CSS

Trang web tin tức Black Friday và xe hơi, bố cục dạng lưới (grid) kết hợp flexbox, có hiệu ứng hover.

🔗 **Demo:** [https://baitap-vtyf.vercel.app/](https://baitap-vtyf.vercel.app/)

## Cấu trúc file
```
bài tập 1/
├── baitap.html    # Nội dung trang
├── style.css      # Toàn bộ định dạng CSS
├── img/           # Ảnh minh họa
└── README.md
```

## Bố cục chính
- **`.news-grid`**: Grid 3 cột chứa 6 tin tức ngắn (ảnh + tiêu đề + ngày)
- **`.featured-articles`**: Flexbox cột chứa 3 bài viết dài (ảnh + tiêu đề + mô tả)
- **`.news-item:hover`**: Card tin tức bật lên nhẹ khi rê chuột vào (transform + transition)
- **Scrollbar tùy chỉnh** cho phần nội dung (chỉ hỗ trợ Chrome/Safari)

## Kỹ thuật CSS sử dụng
Grid Layout, Flexbox, Transition/Transform, `object-fit: cover` cho ảnh, `box-shadow`, `border-radius`.
