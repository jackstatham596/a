<div align="center">

  <img src="assets/SynkroContacts-3D-Banner1.png" alt="SynkroContacts Banner" width="100%" />

  <h1>SynkroContacts</h1>
  <p><b>A modern, fast, offline-first Windows desktop application for managing contacts and companies.</b></p>

  <p>
    <a href="../../releases/latest"><img src="https://img.shields.io/badge/Download-Latest%20Release-0284C7?style=for-the-badge&logo=github&logoColor=white" alt="Download Release" /></a>
    <img src="https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET 8" />
    <img src="https://img.shields.io/badge/Windows-10%20%7C%2011%20(x64)-0078D6?style=for-the-badge&logo=windows11&logoColor=white" alt="Windows" />
    <img src="https://img.shields.io/badge/EF%20Core%20SQLite-8.0.11-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
    <img src="https://img.shields.io/badge/MVVM%20Toolkit-8.3.2-68217A?style=for-the-badge&logo=csharp&logoColor=white" alt="MVVM" />
    <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
  </p>

  <p>
    <a href="#-screenshots">Screenshots</a> •
    <a href="#-features">Features</a> •
    <a href="#-project-structure">Project Structure</a> •
    <a href="#-tech-stack">Tech Stack</a> •
    <a href="#-download--installation">Download &amp; Installation</a> •
    <a href="#-license">License</a>
  </p>

</div>

---

## 📸 Screenshots

<table align="center">
  <tr>
    <th>Blue Theme</th>
    <th>Gold Theme</th>
  </tr>
  <tr>
    <td align="center">
      <img src="assets/contacts-blue.png" alt="Contacts - Blue Theme" width="420" height="260" style="object-fit:cover; width:100%; height:260px;" />
    </td>
    <td align="center">
      <img src="assets/contacts-gold.png" alt="Contacts - Gold Theme" width="420" height="260" style="object-fit:cover; width:100%; height:260px;" />
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="assets/companies-blue.png" alt="Companies - Blue Theme" width="420" height="260" style="object-fit:cover; width:100%; height:260px;" />
    </td>
    <td align="center">
      <img src="assets/SynkroContacts_2.png" alt="Companies - Gold Theme" width="420" height="260" style="object-fit:cover; width:100%; height:260px;" />
    </td>
  </tr>
</table>

---

## ✨ Features

<table>
  <tr>
    <td width="50%" valign="top">
      <b>👥 Linked Contacts &amp; Companies</b><br />
      Associate multiple contacts with a company and navigate seamlessly between a company profile and its people in a single click.
    </td>
    <td width="50%" valign="top">
      <b>📇 Rich, Detailed Profiles</b><br />
      Store multiple phone numbers, email addresses, and physical addresses per contact or company, with the ability to flag your preferred entries.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <b>🔄 vCard (.vcf) Import &amp; Export</b><br />
      Back up or migrate your entire contact list using the industry-standard <code>.vcf</code> format, powered by <code>FolkerKinzel.VCards</code>.
    </td>
    <td width="50%" valign="top">
      <b>🔒 100% Local &amp; Private</b><br />
      No cloud sync, no internet connection required. All data is stored locally in a SQLite database at <code>%AppData%\SynkroContacts\contacts.db</code>.
    </td>
  </tr>
</table>

---

## 🏗 Project Structure

SynkroContacts is built on **.NET 8** (`net8.0-windows10.0.19041.0`) and follows a clean **MVVM architecture** split across five well-defined projects:

```text
SynkroContacts.sln
├── SynkroContacts/             # UI layer — Views, ViewModels, Themes & application startup
├── SynkroContacts.Services/    # Business logic — Contacts, Companies, vCard I/O, logging, notifications
├── SynkroContacts.Data/        # Data access layer — EF Core DbContext, entities & SQLite migrations
├── SynkroContacts.DataMapping/ # Mapping layer — Entity ↔ Model conversion
└── SynkroContacts.Models/      # Core domain models, computed properties & enums
```

---

## 🧰 Tech Stack

| Package | Version | Purpose |
| :--- | :---: | :--- |
| `Microsoft.EntityFrameworkCore.Sqlite` | `8.0.11` | Local SQLite database and schema migrations |
| `CommunityToolkit.Mvvm` | `8.3.2` | MVVM data binding and command infrastructure |
| `FolkerKinzel.VCards` | `7.2.1` | Reading and writing `.vcf` vCard files |

---

## 🚀 Download & Installation

### Option 1 — Download a Pre-built Release *(recommended)*
1. Go to the [**Releases**](../../releases/latest) page.
2. Download the latest `SynkroContacts-win-x64.zip` archive.
3. Extract the archive and run **`SynkroContacts.exe`**.

### Option 2 — Build from Source *(for developers)*

**Requirements:**
- Windows 10 (version 1809+) or Windows 11, `x64`
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) with the **.NET desktop development** workload

**Steps:**
1. Clone the repository:
   ```bash
   git clone https://github.com/jackstatham596/SynkroContacts.git
   cd SynkroContacts
   ```
2. Open **`SynkroContacts.sln`** in Visual Studio 2022.
3. Set the build platform to **`x64`**.
4. Press <kbd>F5</kbd> to build and run.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

<div align="center">
  <img src="assets/SynkroContacts-3D-Icon .png" width="52" />
  <p><sub>Built with ❤️ using C# &amp; .NET 8</sub></p>
</div>
