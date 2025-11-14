# **Ashborne Neon Preset — Setup Guide**

This guide walks you through configuring PowerShell, Starship, and Windows Terminal to use the **Ashborne Neon** aesthetic preset.

---

## 🔧 **1. Verify Your PowerShell Profile**
Check whether your PowerShell profile file exists:

```powershell
Test-Path $PROFILE
```

If it returns **False**, create it:

```powershell
New-Item -Path $PROFILE -ItemType File -Force
```

---

## ✏️ **2. Edit Your PowerShell Profile**
Open the profile file:

```powershell
notepad $PROFILE
```

Add your Starship init line (if not already present):

```powershell
Invoke-Expression (&starship init powershell)
```

---

## 🔓 **3. Allow Your Profile to Run**
Unblock just the profile file:

```powershell
Unblock-File $PROFILE
```

Set execution policy so your user can run local scripts:

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

---

## 🎨 **4. Install / Edit Your Starship Preset**
Open the Starship configuration file:

```powershell
notepad $HOME\.config\starship.toml
```

Paste in the **Ashborne Neon preset** (your custom theme).

---

## 🪟 **5. Configure Windows Terminal**

Press:

**Ctrl + ,**

to open Windows Terminal Settings.

---

## ⚙️ **6. Select the Terminal Profile**
Navigate to:

**Profiles → (Defaults or Windows PowerShell)**  
(depending on whether you want the preset applied globally or only to PowerShell)

---

## 🎨 **7. Appearance Settings**

Inside the profile’s **Appearance** tab, apply the following:

### **Color Scheme**  
- Set to **Dark+** (or your custom Ashborne Neon scheme)

### **Font Face**  
- **FiraCode Nerd Font Mono**

### **Cursor Shape**  
- **Vintage**

### **Background Image**  
- Path: `LogoBW.png`  
- **Background Image Opacity:** `28%`

### **Intense Text Style**  
- Enable **Bold font with bright colors**

### **Background Opacity**  
- **100%**

### **Acrylic Material**  
- Enable Acrylic: **True**

---

## ✔️ Setup Complete
