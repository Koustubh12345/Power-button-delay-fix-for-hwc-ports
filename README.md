# Universal Hardware Composer (HWC) Display Delay Fix 📱⚡

A high-performance, universal script designed to completely eliminate the power button wake delay and touch-to-wake hesitation commonly found on custom Hardware Composer (HWC) vendor ports across Snapdragon devices (such as *sweet*, *alioth*, *munch*, etc.).

---

## 🔥 Features
* **Live ELF Header Injection:** Dynamically patches your device's native `vendor.qti.hardware.display.composer-service` using `patchelf` to load a custom shared library. Bypasses Android's strict `AT_SECURE` capability environmental blocks cleanly.
* **Ultra-Low Response Latency:** Intercepts kernel fence timeout loops (`sync_wait`, `poll`, `ppoll`) and forces them to return instantly within 1ms–5ms.
* **SurfaceFlinger Optimizations:** Injects aggressive property overrides to completely disable hardware backpressure (`latch_unsignaled`) and eliminate framework-level wake delays.
* **100% Device Safe & Universal:** Contains no hardcoded pre-compiled binaries. The script automatically compiles the hook and injects it directly into *your* running device's native composer files live on-device, eliminating any risk of cross-device driver bricking.

---

## 🛠️ Prerequisites

Before executing the script, your device **must** meet the following requirements:

1. **Root Access:** Fully rooted via **KernelSU** or **Magisk**.
2. **Termux App:** Installed and explicitly granted Superuser privileges.
3. **Recommended System Settings:**
   * Turn **OFF** your system's `Pocket mistouch prevention` / `Pocket Mode` in system settings to avoid proximity sensor polling delays.
   * Change your Screen Unlock fingerprint method from **Touch** to **Firm Touch / Press** (if your device uses a physical side-mounted scanner) to force instant mechanical click registration.

---

## 🚀 Installation Instructions

Open **Termux** and copy-paste the commands below to automatically download, build, and apply the live patch:

```bash
# 1. Gain Root Privileges
su

# 2. Download the installation script directly from this repository
curl -sL -o /data/local/tmp/fix_display.sh "[https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/main/fix.sh](https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/main/fix.sh)"

# 3. Execute the script
sh /data/local/tmp/fix_display.sh
