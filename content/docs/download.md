+++
title = "Download"
description = "Download buttons and links for JakeyTTS."
icon = "cloud_download"
weight = 10
+++



You can download the latest pre-compiled version of JakeyTTS or grab the source code using the links below:

* **[Download Installer (.exe)](https://github.com/JakeyTTS/JakeyTTS/releases/download/v2.0.1/JakeyTTS_v2.0.1.exe)**
* **[Windows Download (Releases Page)](https://github.com/JakeyTTS/JakeyTTS/releases)**
* **[Source Code (.zip)](https://github.com/JakeyTTS/JakeyTTS/archive/refs/heads/main.zip)**

---

## 1. System Requirements

Before downloading, please ensure your operating system meets the following specifications:

| Requirement | Minimum | Recommended |
| :--- | :--- | :--- |
| **Operating System** | Windows 10 x64 (Build 19041 or higher) | Windows 11 x64 |
| **Architecture** | 64-bit (x64) | 64-bit (x64) |
| **Runtime** | .NET 8.0 Runtime | .NET 8.0 SDK / Runtime |

---

## 2. Building from Source (Developer Setup)

If you prefer to compile, customize, and run JakeyTTS directly on your machine from the source code, you can set up a local development environment.

### Prerequisites & Tools
* **Visual Studio 2026** (or Visual Studio 2022 v17.8+).
* **.NET 8.0 SDK** (installed automatically with Visual Studio).

### Installation Workloads
During the Visual Studio installation process, you **MUST** select and install the following workloads and components:
1. **.NET Desktop Development** workload.
2. **Windows Application Development** (WinUI / Windows App SDK) modules. Make sure the Windows App SDK templates are checked.

### Compilation Steps
1. Download and extract the **[Source Code (.zip)](https://github.com/JakeyTTS/JakeyTTS/archive/refs/heads/main.zip)** or clone the repository using Git:
   ```bash
   git clone https://github.com/JakeyTTS/JakeyTTS.git
   ```
2. Open the solution file `JakeyTTS.slnx` (or `JakeyTTS.csproj`) in Visual Studio.
3. Wait for NuGet packages to restore automatically.
4. Select the target framework/architecture (e.g., `x64` and `Debug` or `Release`).
5. Press **F5** or click the **Start** button to build and run the application on your device.
