# Universal (HWC) Power Button Delay Fix

A high-performance, universal script designed to completely eliminate the power button wake delay commonly found on custom Hardware Composer (HWC) vendor ports across Snapdragon devices (such as *sweet*, *sweet_k6a*, *vayu*, etc.).

---

## 🔥 Features
* **Advanced Display Hooking:** Cleanly resolves vendor capability and environment blocking issues by implementing a smart, native system-level fix that integrates directly with your device's architecture.
* **Instant Wake Response:** Eliminates deep kernel-level stall cycles and timeout loops, bringing device resume and power button responsiveness down to absolute zero.
* **100% Device Safe & Universal:** Completely automated to match your hardware on the spot. By adapting directly to the active system files on your current device, it guarantees zero compatibility issues and a seamless setup.

---

## 🛠️ Prerequisites

Before executing the script, your device **must** meet the following requirements:

1. **Root Access:** Fully rooted via **KernelSU** or **Magisk**.
2. **Termux App:** Installed and explicitly granted Superuser privileges.

---

## 🚀 Installation Instructions

Open **Termux**, copy the single command block below, paste it, and press enter. It will automatically update your environment, install the compilation utilities, download the patch, and apply it all in one go:

```bash
pkg update -y && pkg upgrade -y && pkg install root-repo -y && pkg install clang patchelf binutils file coreutils grep sed findutils curl -y && curl -sL -o /data/data/com.termux/files/home/script.sh "[https://raw.githubusercontent.com/Koustubh12345/Power-button-delay-fix-for-hwc-ports/main/script.sh](https://raw.githubusercontent.com/Koustubh12345/Power-button-delay-fix-for-hwc-ports/main/script.sh)" && su -c 'sh /data/data/com.termux/files/home/script.sh'
```

Once the setup completes and outputs `=== DONE === REBOOT NOW.`, simply restart your device to enjoy instant screen wake!

---

## 💬 Community & Support

Join our Telegram channels for the latest updates, support, and exclusive releases:

* **[TenSei Mods](https://t.me/TenseiMods)** 
* **[TenSei Channel](https://t.me/GettheFuckoutofhear)** 

---

## 📜 Credits

* **Developer:**([TenSei てんせい](https://t.me/getthefckoutofheree))
