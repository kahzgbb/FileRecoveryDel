# 🧨 FileRecovery Del

A tool written in Go to remove specific directories from **Windows Shadow Copies**, making them unrecoverable by recovery software like NirSoft's *PreviousFileRecovery*.

---

## ✨ Features

- Delete selected folders from **all** system shadow copies  
- Bypass read-only and protected media errors  
- Works on any drive (C:, D:, E:, etc.)  
- Silent and fast execution  

---

## 🧪 How to Use

1. **Run as Administrator**
2. Enter the full path of the directory you want to remove:

```
[ + ] Type the path to exclude: C:\Users\YourName\Downloads\folder
```

3. The program will:

   - Mount all available shadow copies
   - Locate and remove the folder from each copy
   - Clean up mount points automatically

Example output:

```
[ + ] Directory removed from C:\ShadowMounts\C\shadow0
[ + ] Directory removed from C:\ShadowMounts\C\shadow1
[ x ] Failed to remove from shadow2: Media is write-protected
```

---

## ⚠️ Disclaimer

This tool directly deletes data from Windows Shadow Copies (Volume Snapshot Service). Improper use may lead to the loss of system restore points or unintended deletion of critical files. Use it at your own risk and only on directories you fully understand.

---

## 🎫 License
- This project is subject to the [GNU General Public License v3.0](LICENSE). 
