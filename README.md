# Healthcare Alliance — Landing Page Demo (2026)

Chuyển thể trực tiếp từ **Company Profile 2026 – Healthcare Alliance** (25 slide) sang web.

## Cách chạy
Mở `index.html` bằng trình duyệt (cần internet cho Tailwind CDN + Google Fonts).
Bản `healthcare-alliance-landing-standalone.html` là 1 file duy nhất, đã nhúng toàn bộ hình ảnh.

## Nguồn hình ảnh
Toàn bộ logo, chân dung, ảnh dự án, logo khách hàng và icon đối tác dùng **file PNG gốc trong suốt
do khách hàng cung cấp** (thư mục `image-and-icon`), không còn cắt từ ảnh chụp slide:

| Nhóm | Số lượng | Nguồn |
|---|---|---|
| Logo thương hiệu + hệ sinh thái + đối tác | 11 | PNG gốc trong suốt |
| Chân dung (6 advisor + 5 leadership + founder) | 12 | PNG gốc trong suốt |
| Ảnh dự án | 16 | PNG gốc |
| Logo khách hàng (41 y tế + 12 ngoài y tế) | 53 | PNG gốc trong suốt |
| Icon năng lực đối tác (Humiley/Estuary/W&A/AIVISION/Qui Long) | 20 | PNG gốc |
| Icon tròn navy/cam từng section, dải navy 5 business unit | 33 | crop từ slide gốc |

Ảnh đã được nén bằng pngquant (giữ alpha) — tổng assets ~4 MB.

## Bố cục (map 1:1 với profile)
| # | Section | Slide gốc |
|---|---------|-----------|
| 1 | Hero | 1 |
| 2 | Vietnam Healthcare Market | 2 |
| 3 | About Healthcare Alliance | 3 |
| 4 | Vision & Mission | 4 |
| 5 | Our Founder | 5 |
| 6 | Our Leadership | 6 |
| 7 | Our Ecosystem (orbit) | 7 |
| 8 | 5 Business Units (tabs) | 8–12 |
| 9 | Why Healthcare Alliance | 13 |
| 10 | Our Solutions | 14 |
| 11 | Our Impact (counters) | 15 |
| 12 | Our Projects | 16–17 |
| 13 | Strategic Partners (overview + tabs) | 19, 22–25, 28 |
| 14 | Our Clients (53 logo thật) | 29 |
| 15 | Let's Build The Future (contact) | 30 |

## Hệ thống thiết kế
- Navy `#0B315C` · Navy deep `#001C52` · Orange `#E36414` · Orange bright `#FD5B02`
- Font: Montserrat (heading) + Nunito Sans (body)

## Tính năng
- Song ngữ EN/VI (nút EN/VI trên navbar, lưu vào localStorage)
- Scroll reveal, counter animation, parallax hero, orbit xoay, SVG draw-on-scroll
- Tabs cho 5 business unit và 5 đối tác chiến lược
- Click card hệ sinh thái → nhảy thẳng tới tab tương ứng
- Responsive mobile / tablet / desktop, thanh tiến trình đọc, back-to-top
- `prefers-reduced-motion` được tôn trọng

## Trước khi lên production
- Thay Tailwind CDN bằng build Tailwind (`npx tailwindcss -i in.css -o out.css --minify`)
- Self-host font thay vì Google Fonts
- Ảnh hero/ảnh nền section vẫn ở 1366×768 — nếu có bản gốc lớn hơn thì thay để sắc nét hơn trên màn 2K/4K
