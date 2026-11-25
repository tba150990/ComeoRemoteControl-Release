# Hướng dẫn cài đặt & sử dụng WeLAControl trên iPadOS / iOS (`v0.5.4`)

Ứng dụng **WeLAControl iPadOS/iOS `v0.5.4` (Build `54`)** hỗ trợ đồng bộ 1:1 với bản Android: **WeLA Direct LAN / VPN (`TCP 23580`)** + **Windows RDP (`FreeRDP 3`, `TCP 3389`)**, tự động đăng nhập WeLA Remote theo từng máy, quét mạng LAN & OpenVPN 4G/5G, điều khiển màn hình phụ ảo (`ParsecVDD`), âm thanh 48kHz, truyền file 2 chiều và tích hợp đầy đủ mục **Pháp lý & Giấy phép**. *(Tính năng Parsec cũ đã được gỡ bỏ từ v0.5.2+).*

> **Bản quyền:** Copyright © 2026 **@tba150990** (<https://github.com/tba150990>).  
> **Miễn trừ trách nhiệm:** Phần mềm cung cấp theo nguyên trạng (**"AS IS"**). Người dùng tự chịu toàn bộ rủi ro khi cài đặt và sử dụng; xem chi tiết tại [`LICENSE`](LICENSE) và mục **?** -> **Phiên bản & Giấy phép** trong ứng dụng.

---

## 1. Chuẩn bị trước khi cài

### Trên máy tính Windows mục tiêu:
1. **Bật WeLA Direct LAN Host (`v0.5.4`)** *(khuyên dùng — mượt 60–120 FPS, có âm thanh & màn phụ ảo)*:
   - Chạy `WeLA-DirectHost-Setup-v0.5.4.exe` hoặc mở thư mục `WeLA-DirectHost` và chạy `Install-WeLADirectHost.bat` (cài đặt cố định) hoặc `Run-Portable-Now.bat` (chạy ngay không cần cài).
   - Trong tab **Tài khoản & Thiết bị Remote**, tạo sẵn ít nhất một **Tài khoản & Mật khẩu WeLA Remote**.
   - Nếu cần thêm màn hình mở rộng khi kết nối từ iPad/Tablet, mở tab **Quản lý Màn hình phụ** hoặc chạy `Install-Virtual-2nd-Monitor.bat` (cần quyền Administrator lần đầu để cài driver `ParsecVDD`).
2. **Bật Windows Remote Desktop (RDP)** *(tùy chọn dự phòng hoặc dùng tài khoản Windows trực tiếp)*:
   - Vào **Settings -> System -> Remote Desktop** -> **ON** (cổng mặc định `3389`).

### File `.ipa`:
- Tải file `WeLAControl-0.5.4-build54-iPad-unsigned.ipa` từ mục **Releases (`latest`)** trên GitHub của repo (hoặc artifact của workflow `Build WeLAControl iOS IPA`).

---

## 2. Cách cài `.ipa` lên iPad / iPhone

> File `.ipa` xuất từ GitHub Actions là bản **Unsigned** để bạn tự ký bằng Apple ID cá nhân hoặc cài trực tiếp qua TrollStore.

### Cách A: Sideloadly (Windows / macOS — khuyên dùng nếu không dùng TrollStore)
1. Tải [Sideloadly](https://sideloadly.io/), cắm iPad qua cáp USB và nhấn **Tin cậy (Trust)**.
2. Kéo file `WeLAControl-0.5.4-build54-iPad-unsigned.ipa` vào Sideloadly.
3. Nhập Apple ID -> nhấn **Start**.
4. Sau khi cài xong, trên iPad vào **Cài đặt -> Cài đặt chung -> Quản lý VPN & Thiết bị** -> **Tin cậy** chứng chỉ Apple ID của bạn (cần mạng internet để xác minh lần đầu).

### Cách B: TrollStore *(iOS / iPadOS hỗ trợ CoreTrust bug)*
- Chia sẻ/mở file `.ipa` trực tiếp bằng **TrollStore** -> cài đặt vĩnh viễn, không cần gia hạn sau mỗi 7 ngày.

### Cách C: AltStore / SideStore
- Mở file `.ipa` bằng **AltStore** hoặc **SideStore** trên iPad và chọn cài đặt.

---

## 3. Thiết lập & Kết nối lần đầu

1. Khi mở WeLAControl lần đầu, hãy nhấn **Cho phép (Allow)** quyền **Mạng cục bộ (Local Network)** để app quét được PC trong mạng LAN / VPN.
2. Nhấn **+ Thêm thiết bị** trên màn hình chính:
   - **Thông tin kết nối & Cổng:** Nhập tên gợi nhớ, IP LAN hoặc IP VPN (ví dụ Tailscale/OpenVPN/ZeroTier), **Cổng RDP (`3389`)** và **Cổng WeLA LAN (`23580`)**.
   - **Tài khoản WeLA Remote:** Nhập **Tài khoản** và **Mật khẩu** đã tạo trên PC WeLA Host để app **tự động đăng nhập WeLA Direct LAN** ở các lần kết nối tới.
   - **Tài khoản Windows RDP:** Nhập Username / Password Windows (hoặc chọn từ **Kho tài khoản đã lưu**) để dùng cho kết nối RDP.
   - Có thể nhấn nút **Quét LAN / VPN (`UDP 23581`)** ngay trong màn hình chính hoặc trong hộp thoại Direct LAN để tự điền nhanh IP và tên máy (`Alias (HOSTNAME)`).
3. Chạm vào thẻ máy tính để kết nối thông minh (**WeLA Direct LAN -> RDP**), hoặc nhấn trực tiếp nút **Tia sét (WeLA LAN)** / **Màn hình (RDP)**.

---

## 4. Điều khiển & Pháp lý trong ứng dụng

- **Chạm 1 ngón / Di chuyển trên màn:** Di chuyển trỏ chuột & nhấn chuột trái.
- **Chạm giữ:** Mở chuột phải (Right click).
- **Cuộn 2 ngón / Chụm-phóng (Pinch zoom):** Cuộn trang và phóng to/thu nhỏ khung hình.
- **Thanh công cụ nhanh:**
  - **Bàn phím / Phím tắt Windows:** Bật bàn phím iOS, gửi `Ctrl+Alt+Del`, `Win`, `Esc`, `Alt+Tab`, `F1–F12`, hoặc mở **Trackpad ảo**.
  - **Màn hình phụ (Display):** Xem danh sách màn hình hiện có, tạo thêm **Màn hình ảo ParsecVDD**, gỡ màn ảo hoặc chuyển đổi màn hình đang xem tức thì.
  - **Âm thanh (Audio):** Chọn chỉ phát tiếng PC đang mở, phát tất cả hoặc tắt tiếng (48kHz PCM stereo).
  - **Truyền file (Files):** Tải file từ `C:\WeLA-Files` trên Windows về iPad hoặc gửi file từ iPad lên PC.
- **Bản quyền & Giấy phép (`?` -> Phiên bản & Giấy phép):** Xem đầy đủ thông tin bản quyền `@tba150990`, Tuyên bố Từ chối Trách nhiệm và toàn văn giấy phép `FreeRDP`, `OpenSSL`, `parsec-vdd`, `MPL-2.0`, `cJSON`, `uriparser`, `libpng`, `SQLCipher` được đóng gói sẵn trong ứng dụng.
