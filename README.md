# CV Portfolio Website

Website CV/portfolio cá nhân được xây dựng bằng HTML và CSS thuần. Trang web giới thiệu thông tin cá nhân, mục tiêu nghề nghiệp, kỹ năng, công nghệ đã sử dụng và các dự án thực hành.

## Demo

Mở file `index.html` trực tiếp trên trình duyệt hoặc chạy bằng tiện ích Live Server trong VS Code.

## Tính năng chính

- Hiển thị thông tin cá nhân và vị trí ứng tuyển.
- Khu vực giới thiệu bản thân.
- Danh sách kỹ năng, công cụ và công nghệ.
- Khu vực dự án thực chiến kèm hình ảnh minh họa.
- Nút tải CV và điều hướng đến danh sách dự án.
- Giao diện responsive cho nhiều kích thước màn hình.

## Công nghệ sử dụng

- HTML5
- CSS3
- Google Fonts
- Responsive layout
- Static assets: hình ảnh, icon SVG, favicon

## Cấu trúc thư mục

```text
.
├── assets/
│   ├── icons/
│   ├── project*.jpg
│   ├── imgkhoa.png
│   └── rocket-icon.ico
├── css/
│   ├── sections/
│   ├── main.css
│   ├── responsive.css
│   ├── theme.css
│   └── animation.css
├── index.html
├── package-lock.json
└── README.md
```

## Cách chạy dự án

### Cách 1: Mở trực tiếp

1. Tải hoặc clone repository.
2. Mở file `index.html` bằng trình duyệt.

### Cách 2: Dùng Live Server

1. Cài extension **Live Server** trong VS Code.
2. Mở thư mục dự án bằng VS Code.
3. Nhấn chuột phải vào `index.html`.
4. Chọn **Open with Live Server**.

## Tùy chỉnh nội dung

- Thông tin cá nhân: chỉnh trong phần `header` của `index.html`.
- Giới thiệu bản thân: chỉnh trong section `.aboutMe__section`.
- Kỹ năng: chỉnh trong section `.skills__section`.
- Dự án: chỉnh trong section `.projects__section`.
- Hình ảnh và icon: thay thế file trong thư mục `assets/`.
- Giao diện: chỉnh các file CSS trong thư mục `css/`.

## Thêm file CV

Để nút **Tải CV** hoạt động đúng:

1. Đặt file CV vào thư mục `assets/`, ví dụ `assets/cv.pdf`.
2. Cập nhật đường dẫn trong `index.html`:

```html
<a href="./assets/cv.pdf" target="_blank" rel="noopener noreferrer" class="primaryButton" download>
  Tải CV
</a>
```

## Gợi ý triển khai

Dự án là website tĩnh nên có thể deploy miễn phí trên:

- GitHub Pages
- Netlify
- Vercel

## Tác giả

**Trần Đăng Khoa**

- Email: `trandangkhoa2020tv@gmail.com`
- Phone: `0352415850`
