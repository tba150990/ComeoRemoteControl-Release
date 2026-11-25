# Comeo Remote Control (`v0.5.7`)

Ứng dụng điều khiển máy tính Windows từ xa hiệu năng cao dành cho **Android / Tablet** (`v0.5.7`) và **iPadOS / iOS** (tạm giữ bản `v0.5.4`), kết hợp **Comeo Direct LAN / VPN** (60–120 FPS, H.264 GPU, âm thanh 48kHz, màn hình ảo Extend), **Parsec WebRTC** và **Windows RDP (FreeRDP 3)**.

> **Bản quyền:** Copyright © 2026 **@tba150990** (<https://github.com/tba150990>).  
> **Miễn trừ trách nhiệm:** Phần mềm được cung cấp theo nguyên trạng (**"AS IS"**). Người dùng tự chịu mọi rủi ro khi cài đặt và sử dụng — xem chi tiết tại [`LICENSE`](LICENSE) và [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).

---

## Tính năng chính (`v0.5.7`)

- **Đa giao thức kết nối trong một ứng dụng:**
  - **Comeo Direct LAN / VPN (`TCP 23580`):** Stream màn hình độ trễ thấp (H.264 phần cứng GPU + JPEG Zero-Alloc), đồng bộ con trỏ chuột host, âm thanh PCM 48kHz stereo, Clipboard 2 chiều, truyền file 2 chiều tới `Downloads\Comeo-Files`.
  - **Parsec Streaming (`60–120 FPS`):** Tích hợp trực tiếp Parsec WebRTC + 2FA ngay trong app Android hoặc mở App Parsec gốc (`parsec://`), tự động mời đăng nhập khi cần.
  - **Windows RDP (`TCP 3389`):** Tích hợp lõi **FreeRDP 3.33.1** + **OpenSSL 3.3.2** (NLA/TLS, tự khớp Resolution, chia sẻ thư mục `ComeoFiles`, lưu tài khoản Windows cục bộ).
- **Chuyển đổi ngôn ngữ tức thì Tiếng Việt / English (`VI / EN`):** Hỗ trợ đầy đủ cả trên Android và Windows Host (giữ nguyên các thuật ngữ kỹ thuật chuyên ngành khi dùng Tiếng Việt).
- **Quét thiết bị LAN & VPN (`UDP 23581`):** Tự động tìm máy PC trên mạng nội bộ, đồng thời dò `/24` và gateway cho kết nối qua **OpenVPN / 4G / 5G**.
- **Quản lý Màn hình phụ ảo (`ParsecVDD`):** Tạo, gỡ hoặc chuyển đổi trực tiếp giữa màn hình vật lý và các màn hình ảo mở rộng ngay trên thiết bị hoặc trên cửa sổ Host PC.
- **Tài khoản Comeo Remote theo từng thiết bị:** Lưu riêng **Tài khoản / Mật khẩu Comeo Remote** bên cạnh **Tài khoản Windows RDP** và tự động đăng nhập khi kết nối Direct LAN.
- **Comeo Direct LAN Host (`v0.5.7` - Windows):**
  - Đóng gói gọn gồm `ComeoDirectHost.exe` + bộ cài `Install-ComeoDirectHost.bat` / `Comeo-DirectHost-Setup-v0.5.7.exe` và `vdd-driver`.
  - 4 tab quản lý trực quan: *Tài khoản & Thiết bị Remote*, *Quản lý Màn hình phụ (Virtual Display)*, *Cài đặt Thiết bị (Setup PC)* và *Pháp lý & Giấy phép (Legal)*.
- **Minh bạch Pháp lý & Giấy phép:** Tích hợp đầy đủ thông báo bản quyền `@tba150990`, điều khoản từ chối trách nhiệm và toàn văn giấy phép mã nguồn mở (`FreeRDP`, `OpenSSL`, `parsec-vdd`, `nefconw`, `ParsecVDD WHQL`, `AndroidX/Compose`, `MPL-2.0`, `cJSON`, `libpng`, `uriparser`, `SQLCipher`).

---

## Bản quyền, Giấy phép & Miễn trừ trách nhiệm

- **Chủ sở hữu bản quyền:** Copyright © 2026 **@tba150990** (<https://github.com/tba150990>).
- **Thành phần bên thứ ba:** FreeRDP 3.33.1 (Apache 2.0), OpenSSL 3.3.2 (Apache 2.0), parsec-vdd v0.45.1 & Nefarius `nefconw` (MIT), Parsec Virtual Display Adapter Driver (`Root\Parsec\VDA` v0.45 WHQL — Parsec Cloud, Inc.), aFreeRDP JNI (MPL-2.0), AndroidX/Compose/Kotlin (Apache 2.0), cJSON (MIT), uriparser & ios-cmake (BSD 3-Clause), libpng (PNG Reference License), SQLCipher (Zetetic BSD-style).
- **Miễn trừ trách nhiệm:** Phần mềm được cung cấp **"AS IS"**, không kèm bảo đảm. Người dùng tự chịu mọi rủi ro khi cài đặt, mở cổng mạng/Firewall/VPN hoặc vận hành điều khiển từ xa. Xem đầy đủ tại [`LICENSE`](LICENSE).

---

## Kênh tải & Phát hành

Các bản cài đặt chính thức `.apk` (Android ARM64), Windows Host (`.exe` / `.zip`) và `.ipa` (iPadOS Unsigned) được phát hành công khai tại:

- **Kênh tải công khai & In-App Updater:** <https://github.com/tba150990/ComeoRemoteControl-Release/releases/tag/latest>
- **Android (`v0.5.7`):** `ComeoRemoteControl-0.5.7-android-arm64.apk` (hỗ trợ kiểm tra & cập nhật trực tiếp trong app từ repo Public).
- **Windows Host (`v0.5.7`):** `Comeo-DirectHost-Setup-v0.5.7.exe` hoặc `Comeo-DirectHost-Windows-Setup-v0.5.7.zip`.
- **iPadOS (`v0.5.4`):** tạm thời giữ nguyên bản unsigned `.ipa` hiện có.
