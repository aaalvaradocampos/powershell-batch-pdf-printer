# 🖨️ PowerShell Batch PDF Printer

A simple, native PowerShell one-liner designed to automate the repetitive task of printing multiple PDF documents. This script reads all PDF files from a specified folder, sorts them alphabetically by filename, and sends them sequentially to your system's default printer.

## ✨ Features

- **No Third-Party Tools Required:** Uses built-in Windows PowerShell cmdlets (`Start-Process`).
- **Ordered Printing:** Automatically sorts the files by name before printing to ensure your physical documents come out in the correct order.
- **Lightweight:** A single line of code that can be run directly from the console or saved as a `.ps1` script.

## 🚀 How to Use

1. Open **Windows PowerShell** on your computer.
2. Copy the command below.
3. Replace `"C:\Path\To\Your\PDF\Folder"` with the actual path to the folder containing your PDF files.
4. Paste the modified command into PowerShell and press **Enter**.

```powershell
Get-ChildItem -Path "C:\Path\To\Your\PDF\Folder" -Filter *.pdf | Sort-Object Name | ForEach-Object { Start-Process -FilePath $_.FullName -Verb Print }
