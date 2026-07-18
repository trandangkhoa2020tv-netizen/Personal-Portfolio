# CV Portfolio Website

Website CV/portfolio cá nhân của **Trần Đăng Khoa**, được xây dựng bằng HTML5 và CSS3 thuần. Dự án dùng để giới thiệu thông tin cá nhân, định hướng nghề nghiệp, kỹ năng lập trình, kỹ năng mềm và các dự án thực hành trong quá trình học tập.

Trang web hiện là một static website, không cần backend, database hoặc bước build phức tạp. Có thể mở trực tiếp bằng trình duyệt hoặc chạy bằng Live Server trong VS Code.

## Mục tiêu dự án

- Tạo một trang hồ sơ cá nhân trực quan để ứng tuyển vị trí **Backend Developer Intern**.
- Trình bày rõ thông tin liên hệ, giới thiệu bản thân, kỹ năng và dự án đã làm.
- Luyện tập bố cục responsive bằng HTML/CSS thuần.
- Tổ chức CSS theo từng section để dễ bảo trì và mở rộng.
- Sử dụng hình ảnh, icon SVG và hiệu ứng CSS để giao diện sinh động hơn.

## Demo

Cách xem nhanh:

1. Mở file `index.html` trực tiếp trên trình duyệt.
2. Hoặc dùng extension **Live Server** trong VS Code để chạy trang ở môi trường local.

Ví dụ với Live Server:

```text
http://127.0.0.1:5500/index.html
```

Địa chỉ thực tế có thể khác tùy cổng mà Live Server chọn.

## Tính năng chính

- Header hiển thị ảnh đại diện, tên, vị trí ứng tuyển và thông tin liên hệ.
- Section giới thiệu bản thân với lời mô tả ngắn gọn về định hướng học tập và nghề nghiệp.
- Nút tải CV và nút điều hướng nhanh đến danh sách dự án.
- Section kỹ năng gồm:
  - Công cụ và công nghệ: HTML, CSS, JavaScript, React, Node.js, C#, Java, PostgreSQL, Git, MySQL, Docker, SQL Server, Postman.
  - Kỹ năng mềm: giao tiếp, quản lý thời gian, đáng tin cậy, ham học hỏi.
- Section dự án hiển thị 6 project card kèm ảnh minh họa.
- Footer hiển thị tên cá nhân.
- Giao diện responsive cho desktop, tablet và mobile.
- Hiệu ứng CSS:
  - Icon trang trí chuyển động nổi nhẹ.
  - Danh sách logo kỹ năng chạy ngang.
  - Card dự án có hiệu ứng hover.

## Công nghệ sử dụng

- **HTML5**: xây dựng cấu trúc nội dung.
- **CSS3**: style, layout, animation và responsive.
- **CSS variables**: quản lý màu sắc, font size và line height trong `css/theme.css`.
- **CSS Grid/Flexbox**: xây dựng bố cục header, skill grid và project cards.
- **Google Fonts**: sử dụng font `Chakra Petch`.
- **Static assets**: ảnh JPG/PNG và icon SVG.

## Cấu trúc thư mục

```text
.
|-- assets/
|   |-- icons/
|   |   |-- C#.svg
|   |   |-- C.svg
|   |   |-- JS.svg
|   |   |-- css.svg
|   |   |-- docker.svg
|   |   |-- git.svg
|   |   |-- github.svg
|   |   |-- html.svg
|   |   |-- java.svg
|   |   |-- mysql.svg
|   |   |-- nextjs.svg
|   |   |-- node-js.svg
|   |   |-- postgresql.svg
|   |   |-- postman.svg
|   |   |-- react.svg
|   |   `-- sql-server.svg
|   |-- check-icon.svg
|   |-- closed-book.svg
|   |-- grain.jpg
|   |-- graduation-cap-icon.svg
|   |-- imgkhoa.png
|   |-- project.jpg
|   |-- project1.jpg
|   |-- project2.jpg
|   |-- project3.jpg
|   |-- project4.jpg
|   |-- project5.jpg
|   |-- shield-icon.svg
|   |-- skills.jpg
|   |-- sword-icon.svg
|   |-- tom.jpg
|   |-- tombodoi.jpg
|   |-- tomcuoi.jpg
|   |-- tombuonngu2.jpg
|   `-- tree-icon.svg
|-- css/
|   |-- sections/
|   |   |-- about-me.css
|   |   |-- footer.css
|   |   |-- header.css
|   |   |-- projects.css
|   |   `-- skills.css
|   |-- animation.css
|   |-- main.css
|   |-- responsive.css
|   `-- theme.css
|-- index.html
|-- package-lock.json
`-- README.md
```

## Vai trò của các file chính

### `index.html`

File HTML chính của website, chứa toàn bộ nội dung hiển thị trên trang:

- Thẻ `head`: meta viewport, title, CSS chính, favicon và Google Fonts.
- `header`: ảnh đại diện, tên, vị trí ứng tuyển, GitHub, email và số điện thoại.
- `.aboutMe__section`: giới thiệu bản thân và nút CTA.
- `.skills__section`: danh sách công nghệ và kỹ năng mềm.
- `.projects__section`: danh sách project card.
- `footer`: thông tin cuối trang.

### `css/main.css`

File CSS trung tâm, import các file CSS còn lại:

```css
@import "theme.css";
@import "./sections/header.css";
@import "./sections/about-me.css";
@import "./sections/skills.css";
@import "./sections/projects.css";
@import "./sections/footer.css";
@import "./animation.css";
```

Ngoài ra file này còn định nghĩa style nền trang, container, section title và section description.

### `css/theme.css`

Chứa CSS reset, biến màu, gradient và hệ thống typography. Khi muốn đổi màu chủ đạo hoặc kích thước chữ toàn trang, nên chỉnh trong file này trước.

### `css/responsive.css`

Chứa media queries cho các kích thước màn hình:

- `1536px`: giới hạn container cho desktop lớn.
- `1440px`: điều chỉnh layout kỹ năng mềm.
- `1280px`: chuyển header sang dạng cột cho tablet/small laptop.
- `768px`: chuyển skill grid thành một cột.
- `640px`: tối ưu font, padding và about section cho điện thoại.

### `css/animation.css`

Chứa keyframes:

- `float`: hiệu ứng icon bay nhẹ.
- `move-left`: logo kỹ năng chạy sang trái.
- `move-right`: logo kỹ năng chạy sang phải.

### `css/sections/`

Mỗi file phụ trách một phần giao diện riêng:

- `header.css`: layout header, avatar, badge và thông tin liên hệ.
- `about-me.css`: khối giới thiệu bản thân, nút CTA và icon trang trí.
- `skills.css`: skill grid, badge công nghệ và kỹ năng mềm.
- `projects.css`: danh sách project card, ảnh dự án và hover state.
- `footer.css`: style footer.

## Cách chạy dự án

### Cách 1: Mở trực tiếp

1. Tải hoặc clone repository về máy.
2. Mở thư mục dự án.
3. Mở file `index.html` bằng trình duyệt.

### Cách 2: Dùng Live Server trong VS Code

1. Cài extension **Live Server**.
2. Mở thư mục dự án bằng VS Code.
3. Nhấn chuột phải vào `index.html`.
4. Chọn **Open with Live Server**.

### Cách 3: Dùng server tĩnh bất kỳ

Nếu đã có Node.js, Python hoặc công cụ serve static file, có thể chạy một server local trỏ vào thư mục dự án. Dự án không yêu cầu cài dependency vì hiện tại không có package runtime.

Ví dụ với Python:

```bash
python -m http.server 5500
```

Sau đó mở:

```text
http://localhost:5500
```

## Hướng dẫn tùy chỉnh nội dung

### Cập nhật thông tin cá nhân

Mở `index.html` và chỉnh trong phần `header`:

```html
<h2 class="header__title">Đăng Khoa</h2>
<div class="badge">Backend Developer Intern</div>
```

Thông tin liên hệ nằm trong `.header__column--right`:

```html
Github:
Email:
Số điện thoại:
```

### Cập nhật giới thiệu bản thân

Chỉnh nội dung trong section:

```html
<section class="aboutMe__section">
```

Đoạn mô tả chính nằm trong:

```html
<p class="section__description">
```

### Cập nhật kỹ năng công nghệ

Danh sách công nghệ nằm trong các phần tử:

```html
<div class="icon-badges">
  <img src="./assets/icons/html.svg" alt="html icon" />
  <span>html</span>
</div>
```

Khi thêm công nghệ mới:

1. Đặt icon vào `assets/icons/`.
2. Thêm một block `.icon-badges` mới trong `index.html`.
3. Kiểm tra lại giao diện desktop và mobile.

### Cập nhật kỹ năng mềm

Chỉnh các badge trong:

```html
<div class="softSkills__container">
```

Ví dụ:

```html
<div class="softSkills_badge">
  <p>Ham học hỏi</p>
</div>
```

### Cập nhật dự án

Mỗi dự án là một thẻ link trong `.projects__cards_container`:

```html
<a href="" target="_blank" rel="noopener noreferrer">
  <div class="projects_cards">
    <div class="projects__cards_wrapper">
      <img src="./assets/project1.jpg" alt="project1" class="projects__cards_img" />
    </div>
    <div class="projects__cards_titles">
      <h4>dự án 1</h4>
      <h3>Todo List</h3>
    </div>
  </div>
</a>
```

Khi cập nhật project:

1. Đổi `href` thành link GitHub, demo hoặc tài liệu dự án.
2. Đổi ảnh trong `src`.
3. Đổi tên dự án trong thẻ `h3`.
4. Đổi nhãn dự án trong thẻ `h4` nếu cần.
5. Cập nhật `alt` để mô tả ảnh chính xác hơn.

## Thêm file CV

Nút **Tải CV** hiện đang trỏ đến thư mục `assets/`. Để tải đúng file CV, nên đặt file PDF vào `assets/` và cập nhật đường dẫn cụ thể.

Ví dụ:

```text
assets/cv-tran-dang-khoa.pdf
```

Cập nhật trong `index.html`:

```html
<a
  href="./assets/cv-tran-dang-khoa.pdf"
  target="_blank"
  rel="noopener noreferrer"
  class="primaryButton"
  download
>
  Tải CV
</a>
```

## Thay đổi ảnh đại diện

Ảnh đại diện đang được khai báo bằng CSS trong `css/sections/header.css`:

```css
.header__img {
  background-image: url("../../assets/imgkhoa.png");
}
```

Để thay ảnh:

1. Thêm ảnh mới vào `assets/`.
2. Cập nhật đường dẫn `background-image`.
3. Ưu tiên ảnh vuông để avatar không bị cắt xấu.

## Thay đổi màu sắc và font

Màu chủ đạo nằm trong `css/theme.css`:

```css
:root {
  --p-450: hsl(198, 81%, 63%);
  --p-500: hsl(228, 81%, 63%);
  --p-600: hsl(233, 73%, 59%);
}
```

Font chính được import trong `index.html`:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Chakra+Petch:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap"
  rel="stylesheet"
/>
```

Và được áp dụng trong `css/main.css`:

```css
font-family: "Chakra Petch", sans-serif;
```

## Lưu ý kỹ thuật

- Dự án dùng CSS thuần và có sử dụng cú pháp CSS nesting với ký tự `&`.
- Nên kiểm tra trên trình duyệt hiện đại như Chrome, Edge hoặc Firefox phiên bản mới.
- `package-lock.json` hiện không khai báo dependency runtime, vì vậy không cần chạy `npm install` để xem website.
- Các đường dẫn asset đang dùng dạng relative path, ví dụ `./assets/project1.jpg`.
- Khi deploy, nên giữ nguyên cấu trúc thư mục để tránh lỗi mất ảnh hoặc CSS.
- `index.html` đang tham chiếu `assets/rocket-icon.ico` cho favicon và `assets/project6.jpg` cho project thứ 6. Nếu hai file này chưa có trong thư mục `assets/`, cần thêm lại hoặc đổi đường dẫn trước khi deploy.

## Gợi ý kiểm tra trước khi deploy

- Mở trang trên desktop và mobile.
- Kiểm tra ảnh đại diện, ảnh dự án và icon có hiển thị đủ không.
- Kiểm tra nút **Tải CV** đã trỏ đúng file PDF chưa.
- Kiểm tra các link dự án đã có URL thật chưa.
- Kiểm tra `assets/rocket-icon.ico` và `assets/project6.jpg` có tồn tại nếu vẫn giữ các đường dẫn hiện tại trong `index.html`.
- Kiểm tra thông tin liên hệ đã chính xác chưa.
- Kiểm tra font Google Fonts có load được không.
- Kiểm tra giao diện khi mở bằng đường dẫn deploy, không chỉ khi mở local.

## Deploy

Vì đây là static website, có thể triển khai miễn phí trên nhiều nền tảng.

### GitHub Pages

1. Đưa mã nguồn lên GitHub.
2. Vào **Settings** của repository.
3. Chọn **Pages**.
4. Chọn branch deploy, thường là `main`.
5. Chọn thư mục gốc `/root`.
6. Lưu cấu hình và đợi GitHub tạo link Pages.

### Netlify

1. Đăng nhập Netlify.
2. Chọn **Add new site**.
3. Kết nối repository GitHub hoặc kéo thả thư mục dự án.
4. Build command để trống.
5. Publish directory để là thư mục gốc của dự án.

### Vercel

1. Đăng nhập Vercel.
2. Import repository.
3. Framework preset chọn **Other** nếu cần.
4. Build command để trống.
5. Output directory để mặc định nếu deploy từ thư mục gốc.

## Định hướng mở rộng

- Thêm file CV thật và cập nhật nút tải CV.
- Thêm link GitHub/demo cho từng project.
- Bổ sung mô tả ngắn cho mỗi dự án.
- Tách project data sang JavaScript nếu số lượng dự án tăng.
- Thêm dark/light mode nếu muốn cá nhân hóa giao diện.
- Tối ưu `alt` text cho ảnh để cải thiện accessibility.
- Thêm Open Graph meta tags để chia sẻ link đẹp hơn trên mạng xã hội.
- Thêm file `robots.txt` và `sitemap.xml` nếu dùng như portfolio chính thức.

## Tác giả

**Trần Đăng Khoa**

- GitHub: `https://github.com/trandangkhoa2020tv-netizen`
- Email: `trandangkhoa2020tv@gmail.com`
- Phone: `0352415850`
