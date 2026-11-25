# Third-Party Licenses & Legal Notices — WeLAControl

**WeLAControl Suite** (`v0.5.4`)  
**Copyright © 2026 @tba150990** (<https://github.com/tba150990>)  
See [LICENSE](LICENSE) for primary ownership, terms of use, and full warranty/liability disclaimers.

WeLAControl integrates, links against, or distributes the following third-party open-source libraries, build toolchains, and driver packages across **Android (`.apk`)**, **iPadOS/iOS (`.ipa`)**, and **Windows Host (`.exe`)**:

---

## Summary Table of Modules & Licenses

| Component | Platforms | License | Source / Copyright |
| :--- | :--- | :--- | :--- |
| **FreeRDP 3.33.1** (`libfreerdp3`, `libfreerdp-client3`, `libwinpr3`) | Android, iOS | **Apache License 2.0** | <https://github.com/FreeRDP/FreeRDP> |
| **OpenSSL 3.3.2** (`libssl`, `libcrypto`, `OpenSSL.xcframework`) | Android, iOS | **Apache License 2.0** | <https://www.openssl.org> / <https://github.com/krzyzanowskim/OpenSSL> |
| **aFreeRDP Android JNI Integration Heritage** | Android, iOS | **Mozilla Public License 2.0 (MPL-2.0)** | FreeRDP Android JNI / UI heritage |
| **AndroidX, Jetpack Compose & Material 3** | Android | **Apache License 2.0** | Google / The Android Open Source Project |
| **Kotlin Standard Library & Coroutines** | Android | **Apache License 2.0** | JetBrains s.r.o. |
| **parsec-vdd v0.45.1** (`ParsecVDisplay` Virtual Display Core) | Windows, Android, iOS | **MIT License** | Copyright © 2023 Nguyen Duy (<https://github.com/nomi-san/parsec-vdd>) |
| **Parsec Virtual Display Adapter Driver (`Root\Parsec\VDA` v0.45 WHQL)** | Windows Host | **Proprietary WHQL Binary Notice** | Copyright © Parsec Cloud, Inc. (<https://parsec.app>) |
| **Nefarius `nefcon` (`nefconw.exe`)** | Windows Host | **MIT License** | Copyright © Nefarius Software Solutions e.U. (<https://github.com/nefarius/nefcon>) |
| **cJSON 1.7.x** | iOS / FreeRDP | **MIT License** | Copyright © 2009–2017 Dave Gamble and cJSON contributors |
| **libpng 1.6.x** | iOS / FreeRDP | **PNG Reference Library License v2** | <http://www.libpng.org/pub/png/src/libpng-LICENSE.txt> |
| **uriparser 1.0.x** | iOS / FreeRDP | **BSD 3-Clause License** | Copyright © 2007 Weijia Song, Sebastian Pipping |
| **SQLCipher 4.x** | Bundled notice / compatibility | **Zetetic BSD-style License** | Copyright © Zetetic LLC |
| **ios-cmake (`ios.toolchain.cmake`)** | iOS build script | **BSD 3-Clause License** | <https://github.com/leetal/ios-cmake> |

---

## Bundled In-App License Texts

Full verbatim license texts are packaged inside every release artifact:
- **Android APK:** `assets/licenses/` (`WeLA-COPYRIGHT-DISCLAIMER.txt`, `NOTICE.txt`, `FreeRDP-Apache-2.0.txt`, `OpenSSL-Apache-2.0.txt`, `Android-MPL-2.0.txt`, `parsec-vdd-MIT.txt`, `cJSON-MIT.txt`, `libpng-LICENSE.txt`, `uriparser-BSD-3-Clause.txt`, `SQLCipher-LICENSE.md`) and accessible in-app via `?` -> **Pháp lý & Giấy phép**.
- **iPadOS/iOS IPA:** `Resources/assets/licenses/` and `Info.plist` (`NSHumanReadableCopyright`), accessible in-app via `?` -> **Phiên bản & Giấy phép**.
- **Windows Host EXE / Setup:** [`WeLA-DirectHost/THIRD_PARTY_LICENSES.txt`](WeLA-DirectHost/THIRD_PARTY_LICENSES.txt), `WeLADirectHost.exe` assembly copyright metadata, and Tab **Pháp lý & Giấy phép (Legal)** inside the PC Control Center window.

---

## Key Upstream Copyright & Attribution Statements

1. **FreeRDP (Apache License 2.0):**  
   Based on FreeRDP 3.33.1 (`commit 65bcca1913a28cbdd7eb913599f692bd2b707991`). Upstream repository: <https://github.com/FreeRDP/FreeRDP>.
2. **OpenSSL (Apache License 2.0):**  
   Uses OpenSSL 3.3.2 (`https://www.openssl.org`), including Apple platform prebuilds from <https://github.com/krzyzanowskim/OpenSSL> (`3.3.2000`).
3. **parsec-vdd (MIT License):**  
   Copyright (c) 2023 Nguyen Duy <wuuyi123@gmail.com> (<https://github.com/nomi-san/parsec-vdd>).
4. **Parsec Virtual Display Adapter Driver (`Root\Parsec\VDA` v0.45):**  
   The driver files `mm.inf`, `mm.dll`, and `mm.cat` under `WeLA-DirectHost/vdd-driver/driver/` are WHQL-signed binaries copyrighted by **Parsec Cloud, Inc.** (<https://parsec.app>).
5. **Nefarius `nefconw.exe` (MIT License):**  
   Copyright (c) Nefarius Software Solutions e.U. (<https://github.com/nefarius/nefcon>). Used during Windows host setup to install/remove the `Root\Parsec\VDA` device node.
6. **aFreeRDP Android Bridge (MPL-2.0):**  
   Original Android JNI bridge/asset conventions retain Mozilla Public License 2.0 attribution as documented in `Android-MPL-2.0.txt`.
