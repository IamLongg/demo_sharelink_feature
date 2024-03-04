## CÁCH CÁC TỐI ƯU SEO CHO DỰ ÁN SỬ DỤNG REACTJS, NEXTJS

# Triển khai SSR: Server Side Rendering

- Cho phép các công cụ tìm kiếm thu thập thông tin và lập chỉ mục nội dung của trang web tốt hơn vì nội dung HTML được tạo trên máy chủ và các công cụ tìm kiếm có thể dễ dàng truy cập. Điều này có thể dẫn đến SEO tốt hơn và xếp hạng cao hơn cho trang web.
- Ta Sử dụng Static Site Generation (SSG): Next.js cũng hỗ trợ SSG, cho phép tạo ra các trang web tĩnh trước đó được xây dựng và lưu trữ tại máy chủ. Điều này giúp tăng tốc độ tải trang web của bạn và cải thiện trải nghiệm người dùng.
- Giải pháp tốt nhất là nên render html từ phía server gửi về phía client

# Viết Code chuẩn SEO

- Khai báo các thẻ HTML như `<head>`, `<body>`, các thẻ heading,.. chuẩn cấu trúc
- Định dạng các thuộc tính Meta tags như title, description, keywords, author,...
- Dùng nội dung ngắn gọn, đi sâu ý nghĩa
- Responsive phù hợp cho từng thiết bị

# Tốc độ load nhanh

- Tốc độ load nhanh phụ thuộc vào yếu tố sau:

* Quản lý statement chặt chẽ, tránh tình trạng các state bị render trong khi không có update value
* Opimize file build

# Tối ưu performance with ReactJS, NextJS

- Quản lý statement bằng cách sử dụng useMemo, useCallback tránh việc rerender nhiều lần khi không cần thiết
- Dùng phương pháp Virtualiize long lists để hạn chế hiển thị dữ liệu lớn cùng một lúc tránh làm chậm tốc độ load page website (nếu cần)

# Example

# Demo thay đổi tiêu đề, nội dung khi shared link với thẻ Meta Tags

# Cách test :

- Cài đặt extendsion Social Share Preview cho Google Chrome
  ![![alt text](image.png)](public/image.png)
- Open link website bật Social Share Preview extendsion
  ![![alt text](image-1.png)](public/image-1.png)

# Ban đầu thẻ link web hiển thị:

- Code ban đầu:

```js
<head>
  <meta charset="utf-8" />
  <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#000000" />
  <meta name="description" content="Web site created using create-react-app" />
  <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
  <link
    rel="icon"
    href="https://cdn-icons-png.flaticon.com/512/6422/6422200.png"
  />
  <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
  <title>React App</title>
</head>
```

- Title : "React App"
- Description : "Web site created using create-react-app"
- URL : "LOCALHOST:3000"
- Logo: empty

# Thêm thẻ meta trong phần `<head>` để thay đổi title, description, logo

- Code sau khi thêm thuộc tính:

```js
<head>
  <meta charset="utf-8" />
  <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#000000" />
  <meta name="description" content="THIS IS DESCRIPTION" />
  <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
  <link
    rel="icon"
    href="https://cdn-icons-png.flaticon.com/512/6422/6422200.png"
  />
  <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
  <meta
    property="og:image"
    content="https://web4s.vn/uploads/tiny_uploads/tin-tuc/the-meta-trong-html/meta-tag.jpg"
  />
  <title>THIS IS TITLE</title>
</head>
```

# Kết Quả Đạt Được

![![alt text](image-2.png)](public/image-2.png)
