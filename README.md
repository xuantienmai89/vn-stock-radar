# VN-Stock Radar

Dashboard rà soát thị trường chứng khoán Việt Nam — một file HTML duy nhất (`index.html`), chạy hoàn toàn trên trình duyệt.

**Mở:** https://xuantienmai89.github.io/vn-stock-radar/

**Tác giả:** Mai Xuân Tiến · ✉ xuantienmai@gmail.com · ☎ 0906.252.238

3 trang trên máy tính (phím 1 · 2 · 3): **Radar** (lọc & bảng mã) · **Cổ phiếu** (biểu đồ lớn + khớp lệnh + phân tích, nhấp đúp 1 mã ở Radar để mở) · **Thị trường** (chỉ số, VNI ex-Vin, kéo/đè, độ rộng, chỉ số ngành). Mở thẳng: `#cp-FPT`, `#thitruong`.

- **Lớp quyết định (v3.0)**: mỗi mã có 1 trạng thái kèm lý do — ● Điểm mua · ◐ Canh mua · ○ Theo dõi · ▲ Cảnh báo · – Đứng ngoài — gộp từ các cờ Wyckoff/VSA + Ichimoku sẵn có (không thêm công thức mới). Thẻ quyết định: vùng vào (không đuổi quá +3%) · cắt lỗ DG65 & −4% · T1 MA200 · T2 đỉnh 52T · checklist 5 bước. **Công tắc thị trường**: BẬT khi đã có cổ phiếu dẫn dắt (mạnh nhất khi có cả ngành dẫn dắt = ngành ≥4 mã, có ≥2 CP dẫn dắt, ≥3 mã GTGD ≥10 tỷ có Pivot ≤5 phiên, RS ngành ≥50) · TẮT khi chưa có → tỷ trọng thấp, thăm dò cược mã có khả năng dẫn dắt (Loại 1 sát đỉnh). Trong phiên trước 14:45 mọi tín hiệu là *tạm tính* (⏳).
- Dữ liệu thật: bảng giá VPS (5 giây/lần trong phiên) · lịch sử VPS/VNDirect · ngành 24hmoney · cơ bản Simplize (API công khai không chính thức — có thể thay đổi).
- VNI ex-Vin · chỉ số ngành theo vốn hoá · Wyckoff/VSA (port AFL ORION + Loc_TichLuy) · Ichimoku 9·17·26·26 + dao găm 65/129.
- **Khớp lệnh** (trang Cổ phiếu): sổ lệnh 3 bước giá · khớp theo bước giá (mua/bán chủ động, POC, giá TB, vùng 70% KL) · danh sách lệnh khớp, lọc lệnh lớn · intraday mua/bán chủ động 5 phút — nguồn VPS, tự cập nhật 3 giây trong phiên.
- **Biểu đồ Nội bộ**: nút **D · W · M** chuyển nến ngày / tuần / tháng (nến tuần, tháng gộp từ nến ngày VPS, gồm cả phiên đang chạy). D hiển thị tối đa 2 năm gần nhất (3Th · 6Th · 1N · 2N); W và M hiển thị toàn bộ lịch sử (W: 6Th · 1N · 2N · 5N · Max · M: 2N · 5N · 10N · Max). Chế độ MA20/MA50 (tắt nút Ichimoku) mặc định có **dải Bollinger (20, 2)** (nút BB để tắt/bật) và **Mây Ichimoku chuẩn các nền tảng 9·26·52** (Span A = (Tenkan9 + Kijun26)/2, Span B = 52 kỳ, dịch 26). Bật nút Ichimoku → giữ nguyên như cũ: TK9/KJ17/dao găm 65·129/Chikou + Mây theo hệ 9·17·26. Chỉ báo Ichimoku tính trên toàn bộ lịch sử rồi mới cắt khung → khớp AmiBroker. Lăn chuột để phóng to/thu nhỏ, kéo để xem quá khứ, mỗi khung nhớ mức phóng riêng.
- **Biểu đồ Đa khung (v3.2)**: 4 khung cùng lúc theo bố cục AmiBroker — Ngày VSA (EMA6 · EMA10 · MA50 · MA200 · BB20 · volume profile · mũi tên VSA · KL + MA V20/V5) · Tuần / Ngày / Tháng Ichimoku (TK9 · KJ17 · DG65 · DG129 · Mây · Ao Sen · Chikou · dải trạng thái B1, tiêu đề B1/B2/B3, khoảng cách giá–DG65/KJ). Nến tuần/tháng gộp từ nến ngày VPS (gồm cả phiên đang chạy). Lăn chuột phóng to/thu nhỏ cả 4 khung, nhấp đúp về mặc định, ⤢ Phóng to để xem rộng.
- Watchlist/ghi chú lưu trên từng thiết bị (localStorage) — chuyển giữa máy bằng menu ⋯ → *Chuyển sang thiết bị khác (QR)*.
- Điện thoại: mở link → Chia sẻ → *Thêm vào Màn hình chính* để dùng như app.

- **Thanh trượt biểu đồ (v3.6)**: dưới biểu đồ Nội bộ và Đa khung có thanh trượt để kéo về quá khứ (nút ⏭ về hiện tại); ở Đa khung cả 4 khung cùng dời về một mốc ngày, kéo chuột trên biểu đồ cũng được.
- **Màn hình thấp (v3.7)**: trên laptop, phần thông tin dưới biểu đồ (thẻ quyết định, phân tích) hiện đủ chiều cao — lăn chuột ở cột phải để đọc; trang Cổ phiếu: khung Intraday cao cố định, đứng yên khi cuộn.
- **Ngành ở trang Thị trường (v3.8)**: bấm một ngành trong bảng Chỉ số ngành → biểu đồ chuyển sang nến chỉ số ngành dạng VSA (v3.9: O/H/L/C gộp vốn hóa từ các mã trong ngành, cột khối lượng = GTGD tỷ đồng; có EMA6/10, MA50/200, BB, volume profile, mũi tên VSA; ở Đa khung có thêm Tuần/Ngày Ichimoku) và danh sách cổ phiếu của ngành mở ngay dưới dòng đó (quyết định, giá, %, Vol/TB20, RS, GTGD); bấm mã để xem biểu đồ mã tại chỗ, nhấp đúp để mở trang Cổ phiếu, bấm lại tên ngành để đóng.

Không phải khuyến nghị đầu tư.
