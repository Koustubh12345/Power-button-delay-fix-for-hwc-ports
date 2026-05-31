# Universal Hardware Composer (HWC) Display Delay Fix 📱⚡

A high-performance, universal script designed to completely eliminate the power button wake delay and touch-to-wake hesitation commonly found on custom Hardware Composer (HWC) vendor ports across Snapdragon devices (such as *sweet*, *alioth*, *munch*, etc.).

---

## 🔥 Features
* **Advanced Display Hooking:** Cleanly resolves vendor capability and environment blocking issues by implementing a smart, native system-level fix that integrates directly with your device's architecture.
* **Instant Wake Response:** Eliminates deep kernel-level stall cycles and timeout loops, bringing device resume and power button responsiveness down to absolute zero.
* **Framework Optimization:** Permanently cures display backpressure delays and frame-latching hesitation, ensuring smooth, instantaneous power-on transitions.
* **100% Device Safe & Universal:** Completely automated to match your hardware on the spot. By adapting directly to the active system files on your current device, it guarantees zero compatibility issues and a seamless setup.

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
curl -sL -o /data/local/tmp/fix_display.sh "[https://raw.githubusercontent.com/Koustubh12345/Power-button-delay-fix-for-hwc-ports/main/fix.sh](https://raw.githubusercontent.com/Koustubh12345/Power-button-delay-fix-for-hwc-ports/main/fix.sh)"

# 3. Execute the script
sh /data/local/tmp/fix_display.sh
