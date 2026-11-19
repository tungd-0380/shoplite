# ShopLite

ShopLite là một trang thương mại điện tử mini, được xây dựng dần qua từng phiên bản để luyện tập front-end.

## Cấu trúc

- `v1-html/` — Phiên bản 1: HTML semantic + CSS thuần, giao diện tĩnh hoàn chỉnh (tag `v1-html`).
  - `index.html` — Trang danh sách sản phẩm (lưới Grid `auto-fill`, không media query).
  - `product.html` — Trang chi tiết sản phẩm (2 cột desktop, 1 cột mobile).
  - `cart.html` — Trang giỏ hàng (danh sách + khối tổng kết, 2 cột desktop, xếp dọc mobile).
  - `tailwind-card.html` — Bài lab: dựng lại product card bằng Tailwind và đối chiếu class ↔ CSS.
  - `style.css` — CSS dùng chung, toàn bộ màu / spacing / bo góc lấy từ CSS variables.
  - `images/` — Ảnh sản phẩm minh hoạ (SVG).

## Design system

Mọi giá trị thiết kế nằm trong `:root` ở đầu `style.css`:

- Màu: `--color-primary`, `--color-text`, `--color-surface`, …
- Spacing: `--space-1` … `--space-7` (thang 4px)
- Bo góc: `--radius-sm`, `--radius`, `--radius-lg`, `--radius-pill`

Đổi một biến là cả 3 trang đổi theo.

**Dark mode** chỉ ghi đè lại các biến màu (không sửa rule nào khác). Bật bằng:
- nút 🌙 trên header (checkbox + `:has()`, không cần JavaScript), hoặc
- thêm `data-theme="dark"` vào thẻ `<html>`.

## Chạy thử

Mở `v1-html/index.html` trực tiếp trong trình duyệt. Hỗ trợ từ 360px tới desktop.
