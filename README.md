# VN-Stock Radar

Dashboard rà soát thị trường chứng khoán Việt Nam — một file HTML duy nhất (`index.html`), chạy hoàn toàn trên trình duyệt.

**Mở:** https://xuantienmai89.github.io/vn-stock-radar/

3 trang trên máy tính (phím 1 · 2 · 3): **Radar** (lọc & bảng mã) · **Cổ phiếu** (biểu đồ lớn + khớp lệnh + phân tích, nhấp đúp 1 mã ở Radar để mở) · **Thị trường** (chỉ số, VNI ex-Vin, kéo/đè, độ rộng, chỉ số ngành). Mở thẳng: `#cp-FPT`, `#thitruong`.

- **Lớp quyết định (v3.0)**: mỗi mã có 1 trạng thái kèm lý do — ● Điểm mua · ◐ Canh mua · ○ Theo dõi · ▲ Cảnh báo · – Đứng ngoài — gộp từ các cờ Wyckoff/VSA + Ichimoku sẵn có (không thêm công thức mới). Thẻ quyết định: vùng vào (không đuổi quá +3%) · cắt lỗ DG65 & −4% · T1 MA200 · T2 đỉnh 52T · checklist 5 bước. Đèn **công tắc thị trường** (TẮT / THĂM DÒ / GIẢI NGÂN MẠNH) theo số mã dẫn dắt có Pivot ≤5 phiên. Trong phiên trước 14:45 mọi tín hiệu là *tạm tính* (⏳).
- Dữ liệu thật: bảng giá VPS (5 giây/lần trong phiên) · lịch sử VPS/VNDirect · ngành 24hmoney · cơ bản Simplize (API công khai không chính thức — có thể thay đổi).
- VNI ex-Vin · chỉ số ngành theo vốn hoá · Wyckoff/VSA (port AFL ORION + Loc_TichLuy) · Ichimoku 9·17·26·26 + dao găm 65/129.
- **Khớp lệnh** (trang Cổ phiếu): sổ lệnh 3 bước giá · khớp theo bước giá (mua/bán chủ động, POC, giá TB, vùng 70% KL) · danh sách lệnh khớp, lọc lệnh lớn · intraday mua/bán chủ động 5 phút — nguồn VPS, tự cập nhật 3 giây trong phiên.
- **Biểu đồ Nội bộ**: toàn bộ lịch sử ngày (VPS), lăn chuột để phóng to/thu nhỏ, kéo để xem quá khứ, khung 3Th · 6Th · 1N · 2N · 5N · Max.
- Watchlist/ghi chú lưu trên từng thiết bị (localStorage) — chuyển giữa máy bằng menu ⋯ → *Chuyển sang thiết bị khác (QR)*.
- Điện thoại: mở link → Chia sẻ → *Thêm vào Màn hình chính* để dùng như app.

Không phải khuyến nghị đầu tư.
