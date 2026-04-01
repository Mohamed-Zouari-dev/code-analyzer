# Code Analyzer

> A cross-platform desktop application for security auditing, code quality analysis, and compliance checking — fully offline.

---

## What is it?

Code Analyzer is a desktop tool that scans your local projects for security vulnerabilities, code quality issues, and compliance gaps across industry standards. Everything runs **100% on your machine** — your source code never leaves your hands.

---

## Features

- **Security vulnerability detection** via Semgrep (multi-language SAST)
- **Python security analysis** via Bandit
- **Secret & credential leak detection** via Gitleaks
- **Infrastructure-as-Code scanning** via Checkov (Terraform, Kubernetes, Dockerfile)
- **Code smell detection** with a custom built-in engine
- **Quality Score** broken down by Security, Reliability, Maintainability, and Coverage
- **Per-project compliance status** for:
  - OWASP Top 10 (2021)
  - ISO/IEC 27001:2022
  - SOC 2 Type II
- **Scan history** to track your project's security posture over time
- **One-click tool installation** from inside the app

---

## Download

Go to the [Releases page](https://github.com/Mohamed-Zouari-dev/code-analyzer/releases/latest) and download the file for your OS:

| OS | File |
|----|------|
| Windows | `CodeAnalyzer-Windows.exe` |
| macOS | `CodeAnalyzer-macOS` |
| Linux | `CodeAnalyzer-Linux.tar.gz` |

---

## Installation

### Windows
1. Download `CodeAnalyzer-Windows.exe`
2. Double-click to run
3. If Windows Defender shows a warning, click **More info** → **Run anyway**

### macOS
1. Download `CodeAnalyzer-macOS`
2. Open Terminal and run:
```bash
chmod +x CodeAnalyzer-macOS
./CodeAnalyzer-macOS
```
3. If macOS blocks it, go to **System Settings** → **Privacy & Security** → click **Open Anyway**

### Linux
1. Download `CodeAnalyzer-Linux.tar.gz`
2. Extract and run:
```bash
tar -xzf CodeAnalyzer-Linux.tar.gz
cd CodeAnalyzer
./run.sh
```
The launcher script automatically installs any missing dependencies on first run.

---

## Optional: External Scan Tools

The app works out of the box with its built-in engine. For deeper analysis, install these tools:

```bash
pip install semgrep bandit checkov
```

For secret scanning (Gitleaks):
- **macOS**: `brew install gitleaks`
- **Linux**: Download from [gitleaks releases](https://github.com/gitleaks/gitleaks/releases)
- **Windows**: Download from [gitleaks releases](https://github.com/gitleaks/gitleaks/releases)

You can also install tools directly from inside the app on the **Tools** page.

---

## How It Works

1. Open the app and enter or browse to your project folder
2. Click **Start Analysis**
3. The engine runs all available tools in parallel across your codebase
4. Results are displayed with severity levels (Critical, High, Medium, Low)
5. View your **Quality Score**, **Compliance Status**, and **Issue breakdown**
6. All results are saved locally in scan history for future reference

---

## Why Offline?

Your source code is your most valuable asset. Code Analyzer was built from day one to never upload, transmit, or expose your code to any server or cloud service. No telemetry, no accounts, no internet required.

---

## Built With

- **Python** — core engine and backend
- **FastAPI** — local REST API server
- **PyWebView** — native desktop window
- **Semgrep** — static analysis
- **Bandit** — Python security scanning
- **Gitleaks** — secret detection
- **Checkov** — IaC compliance scanning
- **SQLite** — local scan history storage
- **PyInstaller** — cross-platform packaging
- **GitHub Actions** — automated cross-platform builds

---

## Feedback & Contributions

Have a feature request, found a bug, or want to suggest a tool integration? Open an issue or send a message — all feedback is welcome!
