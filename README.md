# 📦 aarch64-linux-android-4.9 Toolchain (For ARM64 Phones)

🔧 A **custom, portable GCC 4.9 toolchain targeting `aarch64-linux-android`**, designed specifically for building directly on ARM64-based Android phones using:

- ✅ [Termux](https://termux.dev/)
- ✅ [Kali NetHunter](https://www.kali.org/kali-nethunter/)
- ✅ Any Linux distribution installed via `chroot` or `proot`

---

## ✨ Features

- ✅ Manually built from source (binutils + GCC 4.9.4)
- ✅ Runs natively on phones without relying on Android system libraries
- ✅ Fully **portable** – no installation or root required
- ✅ Supports building Linux kernels, drivers, and ELF binaries for aarch64
- ✅ Lightweight – ideal for mobile environments like Termux or chroot
- ✅ Tested on real ARM64 devices, no emulators required

---

## 📁 Directory Structure

```
aarch64-linux-android-4.9/
├── bin/            # Toolchain executables: gcc, ld, as, etc.
├── libexec/
├── include/
├── lib/
└── share/
```

---

## 🧪 Requirements

- A phone or device with **ARM64 architecture**
- A Linux environment via:
  - Termux (preferably with `proot-distro`)
  - Kali NetHunter (chroot or proot-based)
  - Any Linux distro installed through `chroot`

---

## 🚀 Quick Usage

```bash
# Add the toolchain to your PATH
export PATH=/path/to/aarch64-linux-android-4.9/bin:$PATH

# Verify it's working
aarch64-linux-android-gcc --version
```

---

## 🧠 Tips

- For best results, use this toolchain inside a `chroot` that contains a proper `libc` and matching headers (e.g., Ubuntu or Kali rootfs).
- When building binaries that require system headers, specify a custom sysroot:
  
  ```bash
  --sysroot=/your/custom/sysroot
  ```

- Ideal for compiling:
  - C/C++ binaries for Android (non-NDK-based)
  - Custom Linux kernel modules
  - AOSP-related binaries for ARM64 targets

---

## ❗ Notes

- This toolchain **does NOT depend on the Android NDK**
- Not recommended for use with `ndk-build` or Android Studio projects

---

## 👨‍💻 Author & Support

Maintained by **Ringo Dz**

For issues, suggestions, or contributions:
- Open an issue on this repository
- Or reach out via:
  - 📧 Email: [youcefrizoug@gmail.com](mailto:youcefrizoug@gmail.com)
  - 💬 Telegram: [https://t.me/youcefrizoug](https://t.me/youcefrizoug)

---

## 🛡️ License

This toolchain was built from open-source components and follows the terms of the **GNU General Public License (GPL v2 or later)**.  
Refer to individual source files for more licensing details.

