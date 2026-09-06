# Bài Tập: Thiết Kế Dạng Trang Web Bằng HTML và CSS

## 📋 Giới Thiệu
Đây là một trang web tin tức về Black Friday và xe hơi, được xây dựng bằng **HTML** và **CSS**. Trang web có bố cục lưới (grid) với hiệu ứng hover tương tác.

🔗 **Demo:** [https://baitap-vtyf.vercel.app/](https://baitap-vtyf.vercel.app/)

---

## 📂 Cấu Trúc File
```
bài tập 1/
├── baitap.html        # File HTML chính
├── style.css          # File CSS (định dạng)
└── README.md          # File hướng dẫn này
```

---

## 🎨 Các Chức Năng Chính

### 1. **Reset CSS - Xóa Margin/Padding Mặc Định**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
- **margin: 0; padding: 0** → Xóa khoảng trắng mặc định của tất cả element
- **box-sizing: border-box** → Tính toán kích thước gồm cả border và padding

**Kết quả:** Layout nhất quán trên tất cả trình duyệt

---

### 2. **Body - Nền Trang**
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
}
```
- **font-family: Arial, sans-serif** → Font chữ là Arial (hoặc sans-serif thay thế)
- **background-color: #f5f5f5** → Nền trang màu xám nhạt

**Kết quả:** Trang web có font chữ đẹp và nền màu xám nhẹ

---

### 3. **Container - Flexbox Layout**
```css
.container {
    display: flex;
    height: 100vh;
    background-color: #ffffff;
}
```
- **display: flex** → Kích hoạt Flexbox
- **height: 100vh** → Chiều cao = toàn bộ chiều cao màn hình
- **background-color: #ffffff** → Nền trắng

**Kết quả:** Container chiếm toàn bộ màn hình

---

### 4. **Header Section - Ẩn**
```css
.header-section {
    display: none;
}
```
- **display: none** → Ẩn phần header (tiêu đề bài tập)

**Kết quả:** Chỉ hiển thị phần nội dung chính

---

### 5. **Content Section - Nội Dung Chính**
```css
.content-section {
    width: 100%;
    background-color: #ffffff;
    padding: 40px;
}
```
- **width: 100%** → Chiếm toàn bộ chiều rộng
- **background-color: #ffffff** → Nền trắng
- **padding: 40px** → Khoảng trắng bên trong 40px (tất cả 4 phía)

**Kết quả:** Nội dung có khoảng trắng thoải mái xung quanh

---

### 6. **Grid Layout - Tin Tức**
```css
.news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin-bottom: 30px;
}
```
- **display: grid** → Kích hoạt Grid Layout
- **grid-template-columns: repeat(3, 1fr)** → Chia thành 3 cột bằng nhau
- **gap: 20px** → Khoảng cách giữa các ô là 20px
- **margin-bottom: 30px** → Khoảng trắng dưới grid

**Kết quả:** 6 tin tức sắp xếp thành 2 dòng, mỗi dòng 3 cột

---

### 7. **Card Tin Tức - News Item**
```css
.news-item {
    background-color: #f9f9f9;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}
```
- **background-color: #f9f9f9** → Nền xám nhạt
- **border-radius: 8px** → Góc bo tròn 8px
- **overflow: hidden** → Ẩn phần nội dung tràn ra ngoài (ảnh tràn khỏi góc tròn)
- **box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1)** → Bóng đổ nhẹ (đen 10%)
- **transition: transform 0.3s ease** → Chuyển động mượt mà trong 0.3 giây

**Kết quả:** Card tin có góc tròn, bóng đổ, và sẵn sàng cho hiệu ứng hover

---

### 8. **Hiệu Ứng Hover - Card Nổi Lên**
```css
.news-item:hover {
    transform: translateY(-5px);
}
```
- **transform: translateY(-5px)** → Bật card lên 5px khi di chuột vào
- Kết hợp với **transition** ở `.news-item` → hiệu ứng mượt mà

**Kết quả:** Khi hover vào tin tức, nó bật lên nhẹ nhàng

---

### 9. **Hình Ảnh Tin Tức**
```css
.news-item img {
    width: 100%;
    height: 220px;
    object-fit: cover;
}
```
- **width: 100%** → Ảnh chiếm toàn bộ chiều rộng container
- **height: 220px** → Chiều cao cố định 220px
- **object-fit: cover** → Ảnh được cắt để vừa khít mà không biến dạng

**Kết quả:** Ảnh hiển thị cân đối, không bị kéo giãn

---

### 10. **Nội Dung Tin Tức - Padding**
```css
.news-item-content {
    padding: 15px;
}
```
- **padding: 15px** → Khoảng trắng bên trong 15px (tất cả 4 phía)

**Kết quả:** Tiêu đề và ngày có khoảng trắng thoải mái

---

### 11. **Tiêu Đề Tin Tức**
```css
.news-item-title {
    font-size: 14px;
    font-weight: bold;
    color: #333;
    margin-bottom: 8px;
    min-height: 40px;
}
```
- **font-size: 14px** → Kích thước chữ 14px
- **font-weight: bold** → Chữ đậm
- **color: #333** → Màu xám đậm
- **margin-bottom: 8px** → Khoảng trắng dưới 8px
- **min-height: 40px** → Chiều cao tối thiểu 40px (giúp tất cả card có chiều cao tiêu đề nhất quán)

**Kết quả:** Tiêu đề hiển thị đậm, rõ ràng và có khoảng cách nhất quán

---

### 12. **Ngày Tháng Tin Tức**
```css
.news-item-date {
    font-size: 12px;
    color: #999;
}
```
- **font-size: 12px** → Kích thước chữ 12px (nhỏ hơn tiêu đề)
- **color: #999** → Màu xám nhạt (không nổi bật như tiêu đề)

**Kết quả:** Ngày tháng hiển thị nhẹ nhàng, không gây lén lút

---

### 13. **Flexbox Layout - Bài Viết**
```css
.featured-articles {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
```
- **display: flex** → Kích hoạt Flexbox
- **flex-direction: column** → Sắp xếp theo chiều dọc (từ trên xuống)
- **gap: 20px** → Khoảng cách giữa các bài viết 20px

**Kết quả:** 3 bài viết xếp chồng lên nhau theo chiều dọc

---

### 14. **Card Bài Viết - Featured Article**
```css
.featured-article {
    display: flex;
    gap: 20px;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}
```
- **display: flex** → Kích hoạt Flexbox (sắp xếp ngang)
- **gap: 20px** → Khoảng cách giữa ảnh và nội dung 20px
- **padding: 20px** → Khoảng trắng bên trong 20px
- **background-color: #f9f9f9** → Nền xám nhạt
- **border-radius: 8px** → Góc bo tròn 8px
- **box-shadow** → Bóng đổ nhẹ

**Kết quả:** Bài viết có ảnh bên trái và nội dung bên phải

---

### 15. **Hình Ảnh Bài Viết**
```css
.featured-article img {
    width: 150px;
    height: 120px;
    object-fit: cover;
    border-radius: 4px;
}
```
- **width: 150px** → Chiều rộng cố định 150px
- **height: 120px** → Chiều cao cố định 120px
- **object-fit: cover** → Ảnh được cắt để vừa khít
- **border-radius: 4px** → Góc bo tròn 4px

**Kết quả:** Ảnh bài viết nhỏ gọn, có góc tròn

---

### 16. **Tiêu Đề Bài Viết**
```css
.featured-article-title {
    font-size: 16px;
    font-weight: bold;
    color: #0066cc;
    margin-bottom: 10px;
}
```
- **font-size: 16px** → Kích thước chữ 16px (lớn hơn tin tức)
- **font-weight: bold** → Chữ đậm
- **color: #0066cc** → Màu xanh dương (nổi bật)
- **margin-bottom: 10px** → Khoảng trắng dưới 10px

**Kết quả:** Tiêu đề bài viết hiển thị xanh dương, bắt mắt

---

### 17. **Danh Mục Bài Viết**
```css
.featured-article-category {
    font-size: 12px;
    color: #999;
    margin-bottom: 8px;
}
```
- **font-size: 12px** → Kích thước chữ 12px (nhỏ)
- **color: #999** → Màu xám nhạt
- **margin-bottom: 8px** → Khoảng trắng dưới 8px

**Kết quả:** Danh mục hiển thị nhẹ nhàng, là thông tin phụ

---

### 18. **Nội Dung Bài Viết**
```css
.featured-article-text {
    font-size: 13px;
    color: #555;
    line-height: 1.4;
}
```
- **font-size: 13px** → Kích thước chữ 13px
- **color: #555** → Màu xám đậm (dễ đọc)
- **line-height: 1.4** → Khoảng cách giữa dòng 1.4 lần font size (dễ đọc)

**Kết quả:** Nội dung dễ đọc, có khoảng cách dòng thoải mái

---

### 19. **Scrollbar Custom - Thanh Cuộn Đẹp**
```css
.content-section::-webkit-scrollbar {
    width: 8px;
}

.content-section::-webkit-scrollbar-track {
    background: #f1f1f1;
}

.content-section::-webkit-scrollbar-thumb {
    background: #888;
    border-radius: 4px;
}

.content-section::-webkit-scrollbar-thumb:hover {
    background: #555;
}
```
- **::-webkit-scrollbar** → Chiều rộng thanh cuộn: 8px
- **::-webkit-scrollbar-track** → Nền track: xám nhạt #f1f1f1
- **::-webkit-scrollbar-thumb** → Thanh cuộn: xám #888, góc tròn 4px
- **::-webkit-scrollbar-thumb:hover** → Khi hover: xám đậm #555

**Kết quả:** Thanh cuộn đẹp, màu sắc phù hợp với design

---

## 📊 Cấu Trúc HTML

```html
<div class="container">
    <div class="content-section">
        <!-- Grid tin tức: 6 items -->
        <div class="news-grid">
            <div class="news-item">
                <img src="1.jpg">
                <div class="news-item-content">
                    <div class="news-item-title">Tiêu đề</div>
                    <div class="news-item-date">Ngày tháng</div>
                </div>
            </div>
            <!-- ... 5 items khác -->
        </div>

        <!-- Bài viết: 3 items -->
        <div class="featured-articles">
            <div class="featured-article">
                <img src="7.jpg">
                <div class="featured-article-content">
                    <div class="featured-article-title">Tiêu đề</div>
                    <div class="featured-article-category">Danh mục</div>
                    <div class="featured-article-text">Nội dung</div>
                </div>
            </div>
            <!-- ... 2 items khác -->
        </div>
    </div>
</div>
```

---

## 🎯 Cách Làm Từng Bước

### Bước 1: Tạo Cấu Trúc HTML
- Tạo container wrapper (flex)
- Tạo content-section chứa toàn bộ nội dung
- Tạo news-grid cho 6 tin tức
- Tạo featured-articles cho 3 bài viết

### Bước 2: Thiết Kế CSS - Grid Tin Tức
```css
.news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```
- Chia thành 3 cột bằng nhau
- Khoảng cách 20px giữa các ô

### Bước 3: Thiết Kế CSS - Card Tin
```css
.news-item {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}
```
- Góc bo tròn
- Bóng đổ nhẹ
- Sẵn sàng cho transition

### Bước 4: Thêm Hiệu Ứng Hover
```css
.news-item:hover {
    transform: translateY(-5px);
}
```
- Card bật lên 5px khi hover
- Chuyển động mượt mà nhờ transition

### Bước 5: Thiết Kế Bài Viết
```css
.featured-article {
    display: flex;
    gap: 20px;
}
```
- Flexbox: ảnh bên trái, nội dung bên phải
- Khoảng cách 20px giữa chúng

### Bước 6: Custom Scrollbar
- Tùy chỉnh thanh cuộn để phù hợp design
- Màu sắc hài hòa với trang web

### Bước 7: Tách CSS Ra File Riêng
- Di chuyển tất cả CSS từ `<style>` vào file `style.css`
- Link file CSS trong HTML: `<link rel="stylesheet" href="style.css">`

---

## 📱 Ghi Chú Thiết Kế
- **Không có media queries** trong phiên bản hiện tại (có thể thêm sau)
- **Không có line-height** trên tiêu đề tin tức (có thể thêm để dễ đọc hơn)
- **Không có text-transform** trên danh mục (có thể thêm `uppercase` để nổi bật)
- **Thanh cuộn custom** chỉ hoạt động trên Chrome/Safari (webkit)

---

## 🎨 Bảng Màu Sắc Sử Dụng
| Tên | Mã Hex | Ứng Dụng |
|-----|--------|---------|
| Trắng | `#ffffff` | Nền chính, container |
| Xám Nhạt (Background) | `#f5f5f5` | Nền body |
| Xám Nhạt (Card) | `#f9f9f9` | Nền card |
| Xám Nhạt (Track) | `#f1f1f1` | Nền track scrollbar |
| Xám Đậm (Chữ) | `#333` | Tiêu đề tin |
| Xám Trung Bình (Phụ) | `#555` | Nội dung bài viết, scrollbar hover |
| Xám Nhạt (Phụ) | `#999` | Ngày tháng, danh mục, scrollbar |
| Xám (Scrollbar) | `#888` | Thanh cuộn |
| Xanh Dương | `#0066cc` | Tiêu đề bài viết |
| Đen Transparent | `rgba(0, 0, 0, 0.1)` | Bóng đổ card |

---

## 💡 Mẹo & Lưu Ý
1. **Transition** luôn đặt ở class gốc (`.news-item`), không phải ở `.hover`
2. **Min-height** giúp các card có chiều cao tiêu đề nhất quán
3. **Object-fit: cover** rất hữu ích cho ảnh responsive
4. **Overflow: hidden** giúp bo tròn hoạt động đẹp với ảnh
5. **Gap** trong grid/flex giúp khoảng cách nhất quán
6. **Box-sizing: border-box** rất quan trọng để tính toán kích thước chính xác

---

## ✨ Kết Luận
Bài tập này sử dụng các kỹ thuật CSS hiện đại:
- ✅ Grid Layout (bố cục lưới 3 cột)
- ✅ Flexbox (bố cục linh hoạt ngang & dọc)
- ✅ Transition & Transform (hiệu ứng hover mượt mà)
- ✅ Object-fit (ảnh responsive)
- ✅ Shadow & Radius (định dạng đẹp)
- ✅ Custom Scrollbar (thanh cuộn tùy chỉnh)

Tạo ra một trang web **chuyên nghiệp, tương tác tốt** trên desktop! 🚀
