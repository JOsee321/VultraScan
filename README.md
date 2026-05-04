```
██╗   ██╗██╗   ██╗██╗  ████████╗██████╗  █████╗ ███████╗ ██████╗ █████╗ ███╗   ██╗
██║   ██║██║   ██║██║  ╚══██╔══╝██╔══██╗██╔══██╗██╔════╝██╔════╝██╔══██╗████╗  ██║
██║   ██║██║   ██║██║     ██║   ██████╔╝███████║███████╗██║     ███████║██╔██╗ ██║
╚██╗ ██╔╝██║   ██║██║     ██║   ██╔══██╗██╔══██║╚════██║██║     ██╔══██║██║╚██╗██║
 ╚████╔╝ ╚██████╔╝███████╗██║   ██║  ██║██║  ██║███████║╚██████╗██║  ██║██║ ╚████║
  ╚═══╝   ╚═════╝ ╚══════╝╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝ ╚═════╝╚═╝  ╚═╝╚═╝  ╚═══╝

        ██████╗ ███████╗██╗   ██╗██╗██╗         ██╗  ██╗██╗██╗     ██╗     ███████╗██████╗
        ██╔══██╗██╔════╝██║   ██║██║██║         ██║ ██╔╝██║██║     ██║     ██╔════╝██╔══██╗
        ██║  ██║█████╗  ██║   ██║██║██║         █████╔╝ ██║██║     ██║     █████╗  ██████╔╝
        ██║  ██║██╔══╝  ╚██╗ ██╔╝██║██║         ██╔═██╗ ██║██║     ██║     ██╔══╝  ██╔══██╗
        ██████╔╝███████╗ ╚████╔╝ ██║███████╗    ██║  ██╗██║███████╗███████╗███████╗██║  ██║
        ╚═════╝ ╚══════╝  ╚═══╝  ╚═╝╚══════╝    ╚═╝  ╚═╝╚═╝╚══════╝╚══════╝╚══════╝╚═╝  ╚═╝

              ██████╗██████╗  █████╗  ██████╗██╗  ██╗███████╗██████╗
             ██╔════╝██╔══██╗██╔══██╗██╔════╝██║ ██╔╝██╔════╝██╔══██╗
             ██║     ██████╔╝███████║██║     █████╔╝ █████╗  ██████╔╝
             ██║     ██╔══██╗██╔══██║██║     ██╔═██╗ ██╔══╝  ██╔══██╗
             ╚██████╗██║  ██║██║  ██║╚██████╗██║  ██╗███████╗██║  ██║
              ╚═════╝╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝
```

<div align="center">

**[ ACUNETIX-CLASS WEB VULNERABILITY SCANNER ]**

**[ BUILT WITH GO | NUCLEI TEMPLATES | ZERO AI | ZERO COST ]**

[![Go Version](https://img.shields.io/badge/Go-1.21+-00ADD8?style=flat-square&logo=go)](https://golang.org)
[![License](https://img.shields.io/badge/License-MIT-red?style=flat-square)](LICENSE)
[![Ethical Use](https://img.shields.io/badge/Use-Ethical%20Only-darkred?style=flat-square)]()

*"We don't break things. We find what's already broken."*

</div>

---

## ⚠️ Peringatan Hukum

> **VultraScan hanya boleh digunakan pada sistem yang kamu miliki atau telah mendapat izin tertulis eksplisit untuk diuji.**
>
> Scanning tanpa izin adalah pelanggaran hukum:
> - 🇮🇩 Indonesia: Pasal 30 UU ITE No. 11 Tahun 2008
> - 🇺🇸 Amerika Serikat: Computer Fraud and Abuse Act (CFAA)
> - 🇬🇧 Inggris: Computer Misuse Act 1990
>
> Developer tidak bertanggung jawab atas penyalahgunaan tool ini.

---

## 📋 Daftar Isi

- [Apa itu VultraScan?](#apa-itu-vultrascan)
- [Mengapa VultraScan?](#mengapa-vultrascan)
- [Arsitektur Pipeline](#arsitektur-pipeline)
- [Struktur Folder](#struktur-folder)
- [Prasyarat](#prasyarat)
- [Instalasi](#instalasi)
- [Konfigurasi](#konfigurasi)
- [Cara Penggunaan](#cara-penggunaan)
- [Nuclei Templates](#nuclei-templates)
- [Authenticated Scanning](#authenticated-scanning)
- [Output & Laporan](#output--laporan)
- [Roadmap Pembangunan](#roadmap-pembangunan)
- [Konsep Go yang Dipelajari](#konsep-go-yang-dipelajari)
- [Kapabilitas Deteksi](#kapabilitas-deteksi)
- [Target Legal untuk Testing](#target-legal-untuk-testing)
- [Kontribusi](#kontribusi)

---

## Apa itu VultraScan?

VultraScan adalah **web vulnerability scanner kelas enterprise** yang dibangun dari nol menggunakan Go. Tool ini dirancang untuk menyamai kemampuan **Acunetix Web Vulnerability Scanner** — yang harganya $7.000/tahun — namun bersifat open source, gratis selamanya, dan sepenuhnya dapat dikustomisasi.

VultraScan menggunakan **Nuclei Templates** dari komunitas ProjectDiscovery — sebuah database ribuan template deteksi kerentanan yang terus diperbarui oleh ribuan security researcher di seluruh dunia. Dengan ini, VultraScan dapat mendeteksi ribuan jenis kerentanan mulai dari XSS sederhana hingga CVE terbaru, tanpa harus menulis template dari nol.

### Apa yang membuat VultraScan berbeda?

| Fitur | VultraScan | Nikto | OWASP ZAP | Acunetix |
|---|---|---|---|---|
| JS Rendering (React/Vue/Angular) | ✅ | ❌ | ⚠️ terbatas | ✅ |
| Authenticated Scanning | ✅ | ⚠️ terbatas | ✅ | ✅ |
| Nuclei Template Support | ✅ | ❌ | ❌ | ❌ |
| Time-Based Blind Detection | ✅ | ❌ | ⚠️ | ✅ |
| OOB Detection (SSRF/Blind RCE) | ✅ | ❌ | ❌ | ✅ |
| Attack Chain Analysis | ✅ | ❌ | ❌ | ❌ |
| CVSS v3.1 Scoring | ✅ | ❌ | ⚠️ | ✅ |
| False Positive Reduction | ✅ | ❌ | ❌ | ✅ |
| Harga | **$0** | $0 | $0 | $7.000/tahun |

---

## Mengapa VultraScan?

### Bagi Security Researcher & Pentester

Bayangkan kamu sedang melakukan pentest. Target menggunakan React SPA — scanner biasa hanya melihat `<div id="root"></div>` yang kosong. VultraScan akan me-render halaman tersebut menggunakan headless Chrome, menunggu semua JavaScript selesai, lalu menganalisis DOM yang sudah terbentuk. Semua endpoint, form, dan AJAX call yang tersembunyi di dalam JavaScript akan ditemukan secara otomatis.

Setelah menemukan endpoint, VultraScan tidak asal-asalan menembak payload. Ia **memilih template Nuclei yang relevan** berdasarkan teknologi yang terdeteksi — WordPress site mendapat WordPress-specific templates, PHP site mendapat PHP templates, dan seterusnya. Ini menghasilkan scan yang lebih akurat dengan lebih sedikit false positive.

### Bagi Developer & Bug Hunter

Kamu sudah menemukan aplikasi yang berjalan di balik login. Scanner gratis lain tidak bisa masuk. VultraScan punya **Auth Engine** yang bisa:
1. Mendeteksi form login otomatis
2. Submit credentials
3. Handle CSRF token
4. Mempertahankan sesi selama scan berlangsung
5. Mendeteksi jika sesi expired dan login ulang otomatis

### Bagi Portofolio

VultraScan adalah bukti bahwa kamu tidak hanya bisa **menggunakan** tools security — kamu bisa **membangunnya**. Dari Go concurrency patterns, Chrome DevTools Protocol, hingga CVSS v3.1 scoring, setiap komponen adalah bukti kemampuan teknis yang nyata.

---

## Arsitektur Pipeline

VultraScan bekerja seperti jalur produksi (assembly line) — output satu fase menjadi input fase berikutnya. Setiap fase bisa berjalan independen, atau dirangkai menjadi satu pipeline penuh.

```
                    ┌──────────────────────────────────────────┐
INPUT ─────────────►│           RECON ENGINE (Week 1)          │
(domain/URL/file)   │  crt.sh · HackerTarget · AlienVault      │
                    │  DNS Resolution · IP Mapping             │
                    └──────────────────┬───────────────────────┘
                                       │ ReconReport
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │           PROBE ENGINE (Week 2)          │
                    │  HTTP/HTTPS · Fingerprint · TLS · WAF    │
                    │  Clickjacking · Security Headers         │
                    └──────────────────┬───────────────────────┘
                                       │ ProbeReport
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │         JS CRAWLER ENGINE (Week 3)       │
                    │  Chromedp Render · Spider Depth-2        │
                    │  Form Extraction · XHR Intercept         │
                    │  Event Trigger · Console Monitor         │
                    └──────────────────┬───────────────────────┘
                                       │ CrawlReport
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │           AUTH ENGINE (Week 4)           │
                    │  Form Login · Session Management         │
                    │  CSRF Token · Bearer Token               │
                    └──────────────────┬───────────────────────┘
                                       │ AuthSession
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │        NUCLEI SCAN ENGINE (Week 5)       │
                    │  Load Templates · Smart Select           │
                    │  Worker Pool · HTTP Sender               │
                    │  Time-Based · Differential · OOB         │
                    │  Two-Pass FP Validation                  │
                    └──────────────────┬───────────────────────┘
                                       │ ScanReport
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │     VULTRA-CORRELATION ENGINE (Week 6)   │
                    │  FP Reducer · Chain Detector             │
                    │  CVSS v3.1 · Severity Adjuster           │
                    │  Remediation Mapper                      │
                    └──────────────────┬───────────────────────┘
                                       │ CorrelationReport
                                       ▼
                    ┌──────────────────────────────────────────┐
                    │          REPORT ENGINE (Week 7)          │
                    │  Interactive HTML · Markdown             │
                    │  CVSS Badge · Attack Chain Viz           │
                    │  Discord/Slack Alert                     │
                    └──────────────────────────────────────────┘
                                       │
                    ┌──────────────────┴───────────────────────┐
                    │              results/                     │
                    │  recon.json · probe.json · scan.json      │
                    │  correlation.json · report.html           │
                    │  report.md                               │
                    └──────────────────────────────────────────┘
```

### Kenapa Pipeline, Bukan Monolith?

Setiap fase adalah package Go yang independen. Artinya:

- Kamu bisa jalankan **hanya recon** tanpa probe atau scan
- Kamu bisa pipe output ke tools lain via JSON
- Testing lebih mudah — setiap package punya unit test sendiri
- Debugging lebih mudah — isolasi masalah per fase

---

## Struktur Folder

```
VultraScan/
│
├── cmd/
│   └── vultrascanner/
│       └── main.go              ← Entry point. Tipis — hanya wiring pipeline
│
├── pkg/
│   ├── config/
│   │   └── config.go            ← Load config.yaml → semua struct config
│   │
│   ├── recon/                   ← Week 1: Subdomain Discovery
│   │   ├── types.go             ← SubdomainResult, ReconReport, Source interface
│   │   ├── engine.go            ← Fan-out/fan-in goroutine orchestrator
│   │   ├── resolver.go          ← DNS worker pool dengan context cancellation
│   │   ├── source_crtsh.go      ← crt.sh Certificate Transparency scraper
│   │   ├── source_hackertarget.go
│   │   └── source_alienvault.go ← AlienVault OTX passive DNS
│   │
│   ├── probe/                   ← Week 2: HTTP Probing & Fingerprinting
│   │   ├── types.go             ← ProbeResult, TLSInfo, ClickjackingResult
│   │   ├── engine.go            ← Worker pool, per-host probing
│   │   ├── http_prober.go       ← HTTP/HTTPS check, redirect chain, title
│   │   ├── fingerprinter.go     ← 30+ technology detection rules
│   │   ├── tls_inspector.go     ← Certificate: expiry, SANs, version, self-signed
│   │   ├── waf_detector.go      ← 15 WAF signature detection
│   │   └── clickjacking_detector.go ← X-Frame-Options + CSP analysis
│   │
│   ├── crawler/                 ← Week 3: JS Crawler Engine
│   │   ├── types.go             ← CrawlResult, Form, XHRRequest, Endpoint
│   │   ├── engine.go            ← Crawler orchestrator, depth control
│   │   ├── renderer.go          ← Chromedp: render JS, wait networkIdle
│   │   ├── spider.go            ← Depth-2 crawl, link follower, dedup
│   │   ├── form_extractor.go    ← goquery: <form>, <input>, <select>
│   │   ├── xhr_interceptor.go   ← CDP Network events, AJAX capture
│   │   ├── event_trigger.go     ← Simulasi klik, expose hidden endpoints
│   │   └── console_monitor.go   ← Browser console error capture
│   │
│   ├── auth/                    ← Week 4: Authentication Engine
│   │   ├── types.go             ← AuthConfig, Session, CookieJar
│   │   ├── engine.go            ← Auth orchestrator
│   │   ├── form_login.go        ← Auto-detect + submit login form
│   │   ├── session_manager.go   ← Cookie persistence, session validation
│   │   ├── token_handler.go     ← Bearer token, CSRF token, API key
│   │   ├── auth_verifier.go     ← Verifikasi login berhasil
│   │   └── scope_filter.go      ← Filter URL yang boleh di-scan
│   │
│   ├── scanner/                 ← Week 5: Nuclei Scan Engine
│   │   ├── types.go             ← NucleiTemplate, Finding, ScanJob
│   │   ├── engine.go            ← Worker pool, job distributor
│   │   ├── template_loader.go   ← Load Nuclei YAML dari disk
│   │   ├── template_selector.go ← Smart selection by tech + severity
│   │   ├── sender.go            ← HTTP request builder + auth injection
│   │   ├── matcher.go           ← Nuclei matchers: word,regex,status,size,dsl
│   │   ├── extractor.go         ← Nuclei extractors: regex, kv, json, xpath
│   │   ├── time_detector.go     ← Time-based blind: median baseline
│   │   ├── differential.go      ← Differential analysis untuk IDOR
│   │   └── interactsh_client.go ← OOB via Interactsh public server
│   │
│   ├── correlation/             ← Week 6: Vultra-Correlation Engine
│   │   ├── types.go
│   │   ├── engine.go
│   │   ├── fp_reducer.go        ← Heuristic false positive reduction
│   │   ├── chain_detector.go    ← Attack chain dari kombinasi findings
│   │   ├── severity_adjuster.go ← Context-aware severity adjustment
│   │   ├── cvss_calculator.go   ← CVSS v3.1 Base Score parser + calculator
│   │   ├── remediation_mapper.go← Tech-specific fix recommendations
│   │   └── rules/
│   │       ├── fp_rules.go
│   │       ├── chain_rules.go
│   │       └── remediation_rules.go
│   │
│   ├── report/                  ← Week 7: Report Engine
│   │   ├── types.go             ← FullReport, RiskScore, CVSS integration
│   │   ├── builder.go           ← Orchestrate semua generator
│   │   ├── html_generator.go    ← Interactive HTML, filter/sort by CVSS
│   │   ├── markdown_generator.go
│   │   └── notifier.go          ← Discord + Slack webhook
│   │
│   └── output/
│       └── writer.go            ← JSON/CSV writers untuk semua fase
│
├── nuclei-templates/            ← Download dari github.com/projectdiscovery/nuclei-templates
│   ├── cves/                    ← CVE-based detection templates
│   ├── vulnerabilities/         ← General vulnerability templates
│   ├── exposures/               ← Sensitive file/data exposure
│   ├── technologies/            ← Technology fingerprinting
│   ├── misconfiguration/        ← Server misconfiguration
│   └── ...
│
├── results/                     ← Output files (gitignored)
│   ├── recon_output.json
│   ├── probe_output.json
│   ├── crawl_output.json
│   ├── scan_output.json
│   ├── correlation_output.json
│   ├── report.html
│   └── report.md
│
├── config.yaml                  ← File konfigurasi utama
├── go.mod
├── go.sum
├── Makefile
├── .gitignore
├── LICENSE
└── README.md
```

---

## Prasyarat

Sebelum menginstall VultraScan, pastikan semua prasyarat berikut sudah terpenuhi:

### 1. Go 1.21 atau lebih baru

```bash
# Cek versi Go yang terinstall
go version
# Output: go version go1.21.x linux/amd64

# Jika belum install, download dari:
# https://go.dev/dl/
```

### 2. Git

```bash
git --version
# Output: git version 2.x.x
```

### 3. Google Chrome atau Chromium

Dibutuhkan untuk JS Crawler Engine (Week 3+). Tanpa ini, scanner tetap bisa berjalan tapi tidak bisa me-render JavaScript.

```bash
# Ubuntu / Debian
sudo apt install chromium-browser

# macOS
brew install --cask google-chrome

# Windows
# Download dari: https://www.google.com/chrome/
# atau Chocolatey: choco install googlechrome
```

### 4. Nuclei Templates (Wajib untuk Scan Engine)

```bash
# Clone nuclei-templates community ke dalam folder project
git clone https://github.com/projectdiscovery/nuclei-templates.git

# Struktur yang diharapkan:
# VultraScan/nuclei-templates/cves/
# VultraScan/nuclei-templates/vulnerabilities/
# dst.
```

> **Kenapa harus clone sendiri?**
> Nuclei templates update setiap hari oleh komunitas. Dengan clone manual, kamu punya kontrol penuh atas template mana yang dipakai, dan bisa `git pull` kapanpun ingin mendapat template terbaru.

---

## Instalasi

### Clone Repository

```bash
# Clone VultraScan
git clone https://github.com/USERNAME/VultraScan.git
cd VultraScan

# Download Nuclei templates ke dalam folder project
git clone https://github.com/projectdiscovery/nuclei-templates.git

# Download Go dependencies
go mod tidy

# Build binary
go build -o vultrascanner ./cmd/vultrascanner/

# Verifikasi
./vultrascanner --help
```

### Build untuk Platform Berbeda

```bash
# Linux (untuk deploy ke VPS/server)
GOOS=linux GOARCH=amd64 go build -o vultrascanner-linux ./cmd/vultrascanner/

# Windows
GOOS=windows GOARCH=amd64 go build -o vultrascanner.exe ./cmd/vultrascanner/

# macOS Apple Silicon
GOOS=darwin GOARCH=arm64 go build -o vultrascanner-darwin ./cmd/vultrascanner/
```

### Development Mode (tanpa build)

```bash
# Jalankan langsung tanpa compile ke binary
go run ./cmd/vultrascanner/ -d example.com
```

---

## Konfigurasi

Semua pengaturan dikontrol melalui satu file: `config.yaml`. Berikut penjelasan lengkap setiap section:

```yaml
# ═══════════════════════════════════════════════════════════════
# VULTRASCAN CONFIGURATION
# ═══════════════════════════════════════════════════════════════

app:
  name: "VultraScan Devil Killer"
  version: "1.0.0"
  # Level log: debug | info | warn | error
  log_level: "info"

# ───────────────────────────────────────────────────────────────
# PHASE 1: RECON ENGINE
# Menemukan semua subdomain dari domain target
# ───────────────────────────────────────────────────────────────
recon:
  # Jumlah goroutine untuk DNS resolution paralel
  # Lebih tinggi = lebih cepat, tapi lebih banyak resource
  concurrency: 50

  # Timeout per DNS query dalam detik
  timeout_seconds: 10

  # Sumber passive recon yang diaktifkan
  # Semua gratis, tidak butuh API key
  sources:
    - crtsh          # Certificate Transparency Logs
    - hackertarget   # HackerTarget API (max 100 req/hari untuk free)
    - alienvault     # AlienVault OTX Passive DNS

  # DNS Bruteforce — lebih lambat tapi lebih lengkap
  bruteforce:
    enabled: false
    wordlist: "wordlists/subdomains-top10000.txt"

  # Hanya simpan subdomain yang berhasil resolve ke IP
  resolve_only: true

  output_file: "results/recon_output.json"

# ───────────────────────────────────────────────────────────────
# PHASE 2: PROBE ENGINE
# Memeriksa setiap subdomain yang ditemukan
# ───────────────────────────────────────────────────────────────
probe:
  # HTTP request lebih berat dari DNS, set lebih rendah dari recon
  concurrency: 20

  timeout_seconds: 10

  # Maksimum redirect yang diikuti
  max_redirects: 5

  # Hanya probe subdomain yang berhasil resolve DNS
  only_resolved: true

  # Aktifkan TLS certificate deep inspection
  enable_tls: true

  output_file: "results/probe_output.json"

# ───────────────────────────────────────────────────────────────
# PHASE 3: JS CRAWLER ENGINE
# Me-render JavaScript dan menemukan attack surface tersembunyi
# ───────────────────────────────────────────────────────────────
crawler:
  enabled: true

  # Kedalaman crawling: 1 = hanya halaman utama, 2 = ikuti link satu level
  # Rekomendasi: 2 (sudah cukup untuk menemukan halaman login dan API utama)
  depth: 2

  # Jumlah tab browser paralel
  # Lebih tinggi = lebih cepat, tapi lebih banyak RAM (~100MB per tab)
  concurrency: 3

  # Timeout per halaman dalam detik
  # React/Vue/Angular butuh waktu lebih lama untuk render
  timeout_seconds: 30

  # Path ke Chrome/Chromium executable
  # Kosong = auto-detect dari PATH
  chrome_path: ""

  # Tampilkan window browser (berguna untuk debugging)
  show_browser: false

  # Skip crawling jika WAF terdeteksi (menghindari IP ban)
  skip_waf_targets: false

  output_file: "results/crawl_output.json"

# ───────────────────────────────────────────────────────────────
# PHASE 4: AUTH ENGINE
# Login ke aplikasi sebelum scanning
# ───────────────────────────────────────────────────────────────
auth:
  # Set true jika target butuh login
  enabled: false

  # URL halaman login
  login_url: "https://example.com/login"

  # Nama field untuk username dan password
  # Kosong = auto-detect dari HTML form
  username_field: ""
  password_field: ""

  # Credentials untuk login
  credentials:
    username: "testuser@example.com"
    password: "testpassword123"

  # String yang muncul di halaman setelah login berhasil
  # Contoh: "dashboard", "Welcome", nama user
  success_pattern: "dashboard"

  # URL untuk validasi sesi masih aktif
  # Biasanya endpoint yang return 401 jika tidak login
  session_check_url: ""

  # Untuk API yang menggunakan Bearer token
  bearer_token: ""

  # Custom headers (untuk API key, dll)
  custom_headers:
    # X-API-Key: "your-api-key-here"

# ───────────────────────────────────────────────────────────────
# PHASE 5: NUCLEI SCAN ENGINE
# Jalankan template Nuclei terhadap attack surface yang ditemukan
# ───────────────────────────────────────────────────────────────
scanner:
  # Jumlah worker goroutine
  # Rekomendasi: 10 (seimbang antara kecepatan dan akurasi)
  concurrency: 10

  timeout_seconds: 10

  # Path ke folder nuclei-templates
  # Relatif dari working directory
  templates_dir: "./nuclei-templates"

  # Filter template berdasarkan severity
  # Kosong = jalankan semua severity
  # Contoh untuk scan cepat: ["critical", "high"]
  severities: []

  # Filter template berdasarkan tags
  # Contoh: ["sqli", "xss", "rce"]
  tags: []

  # Folder/file template yang dikecualikan
  exclude_templates:
    - "nuclei-templates/fuzzing/"  # Terlalu agresif untuk scan reguler

  # Aktifkan time-based blind detection
  # Sedikit memperlambat scan karena butuh baseline measurement
  enable_time_based: true

  # Jumlah request untuk ukur baseline time (lebih banyak = lebih akurat)
  baseline_samples: 5

  # Aktifkan OOB detection via Interactsh public server
  enable_oob: true

  # Aktifkan differential analysis untuk IDOR detection
  enable_differential: true

  output_file: "results/scan_output.json"

# ───────────────────────────────────────────────────────────────
# PHASE 6: VULTRA-CORRELATION ENGINE
# Analisis cerdas tanpa AI — zero cost, zero latency, deterministic
# ───────────────────────────────────────────────────────────────
correlation:
  enabled: true

  # Kurangi false positive menggunakan heuristic rules
  enable_fp_reduction: true

  # Temukan kombinasi findings yang bisa di-chain
  enable_chain_detection: true

  # Sesuaikan severity berdasarkan konteks
  # Contoh: XSS di /admin → Critical, header missing di /api → Info
  enable_severity_adjust: true

  # Hitung CVSS v3.1 Base Score dari vector string di template
  enable_cvss: true

  # Buat remediation plan spesifik per tech stack
  enable_remediation: true

  output_file: "results/correlation_output.json"

# ───────────────────────────────────────────────────────────────
# PHASE 7: REPORT ENGINE
# Generate laporan profesional
# ───────────────────────────────────────────────────────────────
report:
  html_path: "results/report.html"
  markdown_path: "results/report.md"

  # Discord Webhook untuk notifikasi real-time
  # Cara dapat: Server Settings → Integrations → Webhooks → New Webhook
  discord_webhook: ""

  # Slack Incoming Webhook
  # Cara dapat: api.slack.com/apps → Incoming Webhooks
  slack_webhook: ""

  # Minimum severity untuk trigger notifikasi
  # Pilihan: critical | high | medium | low | info
  notify_min_severity: "high"

  # Kirim notif bahkan jika tidak ada finding
  notify_on_empty: false

# ───────────────────────────────────────────────────────────────
# API KEYS (opsional — untuk source premium)
# ───────────────────────────────────────────────────────────────
api_keys:
  securitytrails: ""  # https://securitytrails.com/
  shodan: ""          # https://shodan.io/
  virustotal: ""      # https://virustotal.com/

# ───────────────────────────────────────────────────────────────
# RATE LIMITS
# Requests per second per source — hormati server orang lain!
# ───────────────────────────────────────────────────────────────
rate_limits:
  crtsh: 5
  hackertarget: 2
  alienvault: 5
```

---

## Cara Penggunaan

### Scan Dasar

```bash
# Scan satu domain — jalankan semua fase
./vultrascanner -d example.com

# Scan dengan output lengkap
./vultrascanner -d example.com \
  -oJ results/recon.json \
  -pJ results/probe.json \
  -sJ results/scan.json \
  -html results/report.html
```

### Mode Terbatas

```bash
# Hanya recon (temukan subdomain)
./vultrascanner -d example.com --recon-only

# Recon + probe (tanpa scan)
./vultrascanner -d example.com --probe-only

# Recon + probe + crawl (tanpa scan)
./vultrascanner -d example.com --crawl-only

# Scan cepat — hanya critical dan high
./vultrascanner -d example.com --severity critical,high

# Scan dengan tags tertentu
./vultrascanner -d example.com --tags sqli,xss,rce
```

### Scan Multiple Target

```bash
# Buat file targets.txt
cat > targets.txt << EOF
example.com
test.example.org
# Baris dengan # adalah komentar, akan diabaikan
staging.myapp.com
EOF

# Scan semua target dari file
./vultrascanner -dL targets.txt -html results/report.html
```

### Authenticated Scan

```bash
# Aktifkan auth di config.yaml, lalu:
./vultrascanner -d example.com --auth

# Atau override login URL dari CLI
./vultrascanner -d example.com --auth --login-url https://example.com/signin
```

### Debug Mode

```bash
# Tampilkan browser window saat crawling (debug)
./vultrascanner -d example.com --show-browser

# Skip fase tertentu
./vultrascanner -d example.com --no-crawl --no-headless

# Skip correlation engine
./vultrascanner -d example.com --no-corr

# Skip report generation
./vultrascanner -d example.com --no-report
```

### Semua CLI Flags

| Flag | Tipe | Default | Deskripsi |
|---|---|---|---|
| `-d` | string | — | Target domain tunggal |
| `-dL` | string | — | Path ke file list domain |
| `--config` | string | `config.yaml` | Path ke file konfigurasi |
| `-oJ` | string | dari config | Recon output JSON |
| `-pJ` | string | dari config | Probe output JSON |
| `-sJ` | string | dari config | Scan output JSON |
| `--html` | string | dari config | HTML report path |
| `--md` | string | dari config | Markdown report path |
| `--severity` | string | semua | Filter: `critical,high,medium,low` |
| `--tags` | string | semua | Filter template by tag |
| `--recon-only` | bool | false | Hanya jalankan recon |
| `--probe-only` | bool | false | Jalankan recon + probe |
| `--crawl-only` | bool | false | Jalankan hingga crawler |
| `--auth` | bool | false | Aktifkan authenticated scanning |
| `--no-crawl` | bool | false | Skip JS crawler |
| `--no-corr` | bool | false | Skip correlation engine |
| `--no-report` | bool | false | Skip generate report |
| `--show-browser` | bool | false | Tampilkan browser window |
| `--notify` | bool | false | Kirim notifikasi webhook |

---

## Nuclei Templates

### Apa itu Nuclei Templates?

Nuclei Templates adalah file YAML yang mendefinisikan **satu skenario deteksi kerentanan**. Format ini dibuat oleh ProjectDiscovery dan digunakan oleh ribuan security researcher di seluruh dunia. Template community tersedia gratis di GitHub dan diperbarui setiap hari.

### Struktur Template

```yaml
# Contoh template: CVE-2021-44228 Log4Shell
id: CVE-2021-44228

info:
  name: Log4j RCE — Log4Shell
  author: pdteam
  severity: critical
  description: |
    Apache Log4j2 memiliki kerentanan RCE melalui JNDI lookup.
    Attacker dapat mengeksekusi kode arbitrary di server.
  tags: cve,rce,java,log4j
  cvss-metrics: CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H
  cvss-score: 10.0
  reference:
    - https://nvd.nist.gov/vuln/detail/CVE-2021-44228

requests:
  - method: GET
    path:
      - "{{BaseURL}}"
    headers:
      User-Agent: "${jndi:ldap://{{interactsh-url}}/a}"
      X-Api-Version: "${jndi:ldap://{{interactsh-url}}/a}"
    matchers:
      - type: word
        part: interactsh_protocol
        words:
          - "dns"
```

### Cara Kerja VultraScan dengan Nuclei Templates

1. **Load** — VultraScan membaca semua template `.yaml` dari folder `nuclei-templates/`
2. **Select** — Template dipilih secara cerdas berdasarkan:
   - Teknologi yang terdeteksi di Probe Engine
   - Filter severity dan tags dari config/CLI
   - Exclude list dari config
3. **Execute** — Template dijalankan terhadap semua endpoint dari Crawler Engine
4. **Match** — Response dicocokkan dengan matcher rules di template
5. **Validate** — Two-pass validation untuk kurangi false positive

### Update Templates

```bash
# Update ke template terbaru dari community
cd nuclei-templates
git pull origin main

# Cek template yang baru ditambahkan
git log --oneline -10
```

### Memilih Template yang Aman

Tidak semua template cocok untuk dijalankan di setiap kondisi. Berikut panduan:

```bash
# Untuk scan reguler — gunakan ini
./vultrascanner -d example.com --tags "sqli,xss,ssrf,rce,lfi"

# Untuk CVE detection
./vultrascanner -d example.com --tags "cve"

# JANGAN jalankan ini tanpa izin eksplisit (terlalu agresif)
# --tags "fuzzing"
# nuclei-templates/fuzzing/
```

---

## Authenticated Scanning

Fitur ini memungkinkan VultraScan untuk scan halaman yang berada di balik login.

### Cara Kerja

```
1. VultraScan navigate ke login_url menggunakan Chromedp
2. Auto-detect field username dan password dari HTML form
3. Submit credentials
4. Validasi: cek apakah success_pattern ada di response
5. Simpan session cookies ke CookieJar
6. Inject cookies ke semua request berikutnya (crawler + scanner)
7. Secara berkala validasi sesi masih aktif via session_check_url
8. Jika sesi expired → login ulang otomatis
```

### Contoh Konfigurasi

**Form login standar:**
```yaml
auth:
  enabled: true
  login_url: "https://example.com/login"
  credentials:
    username: "admin@example.com"
    password: "password123"
  success_pattern: "My Dashboard"
```

**API dengan Bearer Token:**
```yaml
auth:
  enabled: true
  bearer_token: "eyJhbGciOiJIUzI1NiIs..."
```

**Aplikasi dengan CSRF Token:**
```yaml
auth:
  enabled: true
  login_url: "https://example.com/login"
  credentials:
    username: "admin"
    password: "password"
  # VultraScan otomatis extract dan inject CSRF token
  success_pattern: "Welcome, Admin"
```

---

## Output & Laporan

### JSON Outputs

Setiap fase menghasilkan JSON yang bisa diproses oleh tools lain:

```bash
# Contoh: proses dengan jq
cat results/scan_output.json | jq '.findings[] | select(.severity=="critical")'

# Export findings ke CSV custom
cat results/scan_output.json | jq -r '.findings[] | [.name,.severity,.url] | @csv'
```

### HTML Report

File `results/report.html` adalah laporan self-contained yang bisa dibuka tanpa internet. Fitur:

- **Filter by severity** — tampilkan hanya Critical, atau semua
- **Sort by CVSS score** — finding paling berbahaya tampil pertama
- **Evidence expandable** — klik untuk lihat HTTP request + response snippet
- **Attack chain visualization** — lihat bagaimana findings bisa di-kombinasikan
- **CVSS v3.1 badge** — setiap finding punya score dan vector string
- **Remediation guide** — kode contoh fix spesifik untuk tech stack target

### Notifikasi Real-time

Saat VultraScan menemukan finding critical atau high, notifikasi langsung dikirim ke Discord/Slack dengan format:

```
🚨 VultraScan Alert — example.com
━━━━━━━━━━━━━━━━━━━━━━━━━━
Risk Score: 87/100 (Critical)
━━━━━━━━━━━━━━━━━━━━━━━━━━
🔴 CRITICAL: SQL Injection — Error Based
   URL: https://api.example.com/?id='
   CVSS: 9.8 (AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)

🔴 CRITICAL: Log4Shell (CVE-2021-44228)
   URL: https://example.com/
   CVSS: 10.0

⛓ Attack Chain Detected:
   [CRITICAL] Database Dump → Admin Takeover
```

---

## Roadmap Pembangunan

| Week | Modul | Status | Deskripsi |
|---|---|---|---|
| 1 | Recon Engine | 🔜 Soon | Passive subdomain discovery |
| 2 | Probe Engine | 🔜 | HTTP probing + fingerprinting |
| 3 | JS Crawler Engine | 🔜 | Chromedp rendering + form extraction |
| 4 | Auth Engine | 🔜 | Authenticated scanning |
| 5 | Nuclei Scan Engine | 🔜 | Template-based scanning + OOB |
| 6 | Vultra-Correlation | 🔜 | FP reduction + CVSS + chains |
| 7 | Report Engine | 🔜 | Interactive HTML + notifications |

### Git Flow

Setiap week mengikuti pola yang sama:

```bash
# Selama development
git add .
git commit -m "wip(weekN): deskripsi progress"

# Setelah week selesai dan semua test pass
git add .
git commit -m "feat(weekN): deskripsi fitur utama

- File baru: ...
- File diubah: ...
- Dependency baru: ..."

git tag vX.X.0-weekN
git push origin main --tags
```

---

## Konsep Go yang Dipelajari

Setiap week mengajarkan konsep Go yang berbeda — dari yang dasar hingga advanced.

### Week 1 — Goroutines & Channels
Goroutine adalah unit concurrency Go yang sangat ringan (~2KB RAM vs ~1MB untuk OS thread). Channel adalah cara aman untuk komunikasi antar goroutine.

```go
// Fan-Out: satu domain → banyak source berjalan paralel
for _, source := range sources {
    source := source  // capture loop variable!
    go func() {
        defer close(ch)
        source.Fetch(domain, ch, done)
    }()
}

// Fan-In: gabungkan semua channel menjadi satu
merged := mergeChannels(done, ch1, ch2, ch3)
for result := range merged {
    process(result)
}
```

### Week 2 — Interface Implisit
Di Go, interface dipenuhi secara implisit — tidak ada `implements` keyword.

```go
type Source interface {
    Fetch(domain string, results chan<- Result, done <-chan struct{})
    Name() string
}
// Struct apapun yang punya kedua method ini otomatis implement Source
```

### Week 3 — Chrome DevTools Protocol
Chromedp adalah Go binding untuk CDP — protokol yang digunakan browser untuk komunikasi antara devtools dan browser engine.

```go
// Listen untuk network requests sebelum navigasi
chromedp.ListenTarget(ctx, func(ev interface{}) {
    if req, ok := ev.(*network.EventRequestWillBeSent); ok {
        captureXHR(req)
    }
})
```

### Week 4 — Context & Cancellation
Context adalah cara standar Go untuk propagate cancellation dan deadline.

```go
ctx, cancel := context.WithTimeout(context.Background(), 30*time.Second)
defer cancel()  // WAJIB — mencegah goroutine leak

chromedp.Run(ctx,
    chromedp.Navigate(loginURL),
    chromedp.WaitReady("body"),
)
```

### Week 5 — sync/atomic & Worker Pool
`sync/atomic` untuk counter yang diakses banyak goroutine tanpa mutex overhead.

```go
var totalRequests atomic.Int64

// Di setiap worker goroutine
totalRequests.Add(1)  // Lock-free, operasi CPU instruction
```

### Week 6 — Pure Functions & Testability
Semua rule engine diimplementasikan sebagai pure functions — input yang sama selalu menghasilkan output yang sama. Ini membuat semuanya mudah di-test.

```go
// Pure function: tidak ada side effect, deterministic
func EvaluateFPRules(input FPRuleInput) (score int, rules []FPRuleResult) {
    // ...
}
```

### Week 7 — Template Rendering
Generate HTML report yang kompleks menggunakan Go's `html/template`.

---

## Kapabilitas Deteksi

### Teknologi yang Dideteksi (30+)

| Kategori | Teknologi |
|---|---|
| Web Server | Nginx, Apache, IIS, Caddy, LiteSpeed, OpenResty |
| Bahasa | PHP (dengan versi), ASP.NET, Python |
| Framework | Express.js, Next.js, React, Vue.js, Angular, Nuxt.js, Laravel, Django, Flask |
| CMS | WordPress, Drupal, Joomla, Magento |
| E-Commerce | Shopify, WooCommerce, PrestaShop |
| CDN | Cloudflare, AWS CloudFront, Fastly, Akamai |
| Hosting | Vercel, Netlify, GitHub Pages |

### WAF yang Dideteksi (15)

Cloudflare, AWS WAF, Akamai, Sucuri, Imperva, F5 BIG-IP, ModSecurity, Barracuda, Fastly, Varnish, StackPath, Wordfence, Alibaba Cloud WAF, Fortiweb, Radware

### Jenis Kerentanan (via Nuclei Templates)

| Kategori | Contoh |
|---|---|
| Injection | SQL Injection, Command Injection, LDAP Injection |
| XSS | Reflected, Stored, DOM-based |
| SSRF | Basic, Cloud Metadata, Blind via OOB |
| RCE | Log4Shell, Spring4Shell, arbitrary code execution |
| LFI/RFI | Local/Remote file inclusion |
| XXE | XML External Entity |
| Open Redirect | Parameter-based redirect |
| IDOR | Insecure Direct Object Reference |
| Authentication | Default credentials, auth bypass |
| Misconfiguration | Exposed admin panels, debug endpoints |
| Exposures | `.env` files, backup files, git exposure |
| CVEs | Ribuan CVE terbaru dari community templates |

---

## Target Legal untuk Testing

**Gunakan target berikut untuk belajar dan testing — semuanya legal dan sengaja disediakan untuk tujuan ini:**

```bash
# testphp.vulnweb.com — Acunetix demo target, sengaja vulnerable
./vultrascanner -d testphp.vulnweb.com

# scanme.nmap.org — milik Nmap project
./vultrascanner -d scanme.nmap.org --recon-only

# hack.me — platform CTF legal
./vultrascanner -d hack.me

# localhost — VM/Docker vulnerable apps
# DVWA: github.com/digininja/DVWA
# Juice Shop: github.com/juice-shop/juice-shop
# WebGoat: github.com/WebGoat/WebGoat
docker run -d -p 80:80 vulnerables/web-dvwa
./vultrascanner -d localhost
```

---

## Kontribusi

Kontribusi sangat disambut! Cara berkontribusi:

```bash
# 1. Fork repository ini
# 2. Buat branch untuk fitur/fix kamu
git checkout -b feat/nama-fitur

# 3. Commit dengan format yang benar
git commit -m "feat(modul): deskripsi singkat"

# 4. Push dan buat Pull Request
git push origin feat/nama-fitur
```

### Cara Menambah Sumber Recon Baru

Cukup implementasikan interface `Source`:

```go
type MyNewSource struct{}

func (s *MyNewSource) Name() string { return "mynewsource" }
func (s *MyNewSource) Fetch(domain string, results chan<- SubdomainResult, done <-chan struct{}) {
    // implementasi
}
```

### Cara Menambah Chain Rule Baru

Edit `pkg/correlation/rules/chain_rules.go` dan tambahkan entry baru di `AllChainRules`. Tidak perlu ubah engine.

---

## Lisensi

VultraScan dirilis di bawah lisensi MIT. Lihat [LICENSE](LICENSE) untuk detail.

---

<div align="center">

**Built with ❤️ and Go**

*"The difference between a tool and a weapon is authorization."*

</div>