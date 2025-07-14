
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

## 🔻 Step 1: Download Windows 11 24H2 ISO (Official)

### ✔️ One-Click Direct Link (English - x64 ISO)
➡️ [Download Windows 11 24H2 ISO (Official Link)](https://software.download.prss.microsoft.com/dbazure/Win11_24H2_English_x64v1.iso)

> 💡 *This is a direct link from Microsoft servers. It may expire; regenerate via [Microsoft ISO page](https://www.microsoft.com/en-us/software-download/windows11).*

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

## 🛠️ Step 3: Manual Bypass (Optional)

### Method 1: Delete or Patch `appraiserres.dll`

1. Mount the Windows ISO
2. Copy contents to a new folder (e.g., `C:\Win11`)
3. Delete this file:
```plaintext
C:\Win11\sources\appraiserres.dll
```
4. Run setup or recreate ISO (optional)

### Method 2: Use Registry (`LabConfig`) Hack

1. During setup, press **Shift + F10** to open CMD
2. Type `regedit` and go to:
```
HKEY_LOCAL_MACHINE\SYSTEM\Setup
```
3. Create key `LabConfig`
4. Add these values:

| Name | Type | Value |
|------|------|-------|
| BypassTPMCheck | DWORD | 1 |
| BypassRAMCheck | DWORD | 1 |
| BypassSecureBootCheck | DWORD | 1 |

---

## 🚀 Step 4: Start Windows Installation

- Boot from USB or run `setup.exe`
- Choose **Custom Installation**
- Format the desired partition
- Begin install — TPM, Secure Boot, RAM errors should be gone!

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
| 1️⃣ | Download Windows 11 24H2 ISO (Official) |
| 2️⃣ | Use Rufus 4.7 to create bootable USB with bypass |
| 3️⃣ | (Optional) Patch appraiserres.dll or use LabConfig Registry |
| 4️⃣ | Install Windows on unsupported hardware |
| 5️⃣ | Download & install missing drivers |

---

## 📎 Notes

- 2GB RAM is the **bare minimum** — consider Tiny11 or debloated builds for better performance.
- Rufus bypass method is the **easiest and safest**.
- Direct ISO links may expire after a few days — always regenerate from official source.

---

Happy Installing! 🎉
