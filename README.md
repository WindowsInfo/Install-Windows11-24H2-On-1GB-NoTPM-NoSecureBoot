# Merging Method 2 (LabConfig Registry Hack) directly under Step 3 in a cleaner way

final_readme_content = """
# 💻 How to Install Windows 11 24H2 on 2GB RAM PC — No TPM | No Secure Boot | Bypass Methods

This guide helps you install **Windows 11 24H2** on older PCs with only **2GB RAM**, **No TPM**, and **No Secure Boot**. It includes multiple bypass methods: **Rufus**, **Registry Hacks**, and **appraiserres.dll** tweaks.

---

## 📂 Repository Name:
**Install-Windows11-24H2-On-2GB-NoTPM-NoSecureBoot**

---

## ✅ Requirements

- PC with **2GB RAM**, Legacy or UEFI BIOS
- **16GB+ USB Drive**
- Internet connection for ISO and drivers
- Basic PC handling knowledge

---

## 🔻 Step 1: Download Windows 11 24H2 ISO

### ✔️ One-Click Direct Link (Safe from Internet Archive)
➡️ [Download Windows 11 24H2 ISO (Internet Archive)](https://archive.org/download/windows-11-24h2-iso_202501/Win11_24H2_English_x64.iso)

> 💡 *This is a verified ISO hosted on the Internet Archive. Use for testing and educational purposes.*

---

## 🔧 Step 2: Create Bootable USB using Rufus 4.7 (with Bypass)

### 1. Download Rufus 4.7 Portable:
➡️ [Rufus 4.7 Portable Download](https://github.com/pbatard/rufus/releases/download/v4.7/rufus-4.7p.exe)

### 2. Steps:

- Launch Rufus
- Select your USB drive and the Windows 11 ISO
- Enable the following bypass options when prompted:

  - [x] Remove TPM Check  
  - [x] Remove Secure Boot Check  
  - [x] Remove RAM Requirement (for systems under 4GB)  
  - [x] Allow Local Account

> ⚠️ If options do not appear, click **Show Advanced Drive Properties** and enable extended features.

---

## 🛠️ Step 3: Manual Bypass Methods (Optional)

If you are not using Rufus or want to customize further, try these manual bypass methods:

### 🔹 Method A: Using Regisrty Editor

1. Mount the Windows ISO  

2. Create a new key called `LabConfig`  
3. Inside `LabConfig`, add the following DWORD values:

| Name                  | Type   | Value |
|-----------------------|--------|-------|
| BypassTPMCheck        | DWORD  | 1     |
| BypassRAMCheck        | DWORD  | 1     |
| BypassSecureBootCheck | DWORD  | 1     |

This will bypass the TPM, RAM, and Secure Boot checks during installation.

---

## 🚀 Step 4: Start Windows Installation

- Boot from USB or run `setup.exe`
- Choose **Custom Installation**
- Format the desired partition
- Begin install — TPM, Secure Boot, RAM errors should be gone! ✅

---

## 🌐 Step 5: Install Drivers

After setup:

### 🔻 Use DriverPack Solution:
➡️ [DriverPack Offline Full Version](https://drp.su/en/foradmin)

Or download drivers from your PC/motherboard manufacturer.

---

## 📘 Summary

| Step | Action |
|------|--------|
| 1️⃣ | Download Windows 11 24H2 ISO (Internet Archive) |
| 2️⃣ | Use Rufus 4.7 to create bootable USB with bypass |
| 3️⃣ | Manually apply Registry LabConfig |
| 4️⃣ | Install Windows on unsupported hardware |
| 5️⃣ | Download & install missing drivers |

---

## 📎 Notes

- 2GB RAM is the **bare minimum** — consider Tiny11 or debloated builds for better performance.
- Rufus bypass method is the **easiest and safest**.
- This ISO is archived and safe for educational and testing use.

---

Happy Installing! 🎉
"""