# quanlytool — GitHub Pages

Đây là **frontend tĩnh** để upload lên GitHub Pages.

## File quan trọng

- `index.html` — trang chính GitHub Pages.
- `api-config.js` — URL của license API.
- `.nojekyll` — yêu cầu GitHub Pages phục vụ file tĩnh trực tiếp.
- `admin.html` — redirect về `index.html`.

## Upload

Đưa toàn bộ file trong thư mục này lên **root của branch `main`**.

Trong GitHub:

`Settings -> Pages -> Deploy from a branch -> main -> /(root)`

URL của repo `quanlytool` sẽ có dạng:

`https://lecongminhvuong31154-hash.github.io/quanlytool/`

## Trước khi nối backend

Web vẫn mở và hiển thị giao diện ở chế độ xem trước.

## Khi đã có server API

Sửa `api-config.js`:

```js
window.APP_CONFIG = {
  API_BASE_URL: "https://api.tenmiencuaban.com",
  API_TIMEOUT_MS: 8000
};
```

Không đặt mật khẩu admin, KEY khách hoặc database trong `api-config.js`.

## CORS trên server

Backend phải cho phép origin:

`https://lecongminhvuong31154-hash.github.io`

Backend mẫu trong gói private đi kèm đã hỗ trợ việc này.
