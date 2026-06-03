# Tugas Akhir: n8n Workflow Automation

<div align="center">

![n8n](https://img.shields.io/badge/n8n-workflow_automation-red?style=flat-square&logo=n8n)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![Status](https://img.shields.io/badge/status-active-green?style=flat-square)

</div>

## 📋 Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Fitur Utama](#fitur-utama)
- [Prasyarat](#prasyarat)
- [Instalasi](#instalasi)
- [Penggunaan](#penggunaan)
- [Struktur Proyek](#struktur-proyek)
- [Workflow Details](#workflow-details)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)
- [Kontak](#kontak)

## 🎯 Tentang Proyek

Proyek Tugas Akhir ini merupakan implementasi workflow automation menggunakan **n8n** (an extendable workflow automation platform) dengan fokus pada **NFA (Non-deterministic Finite Automaton)** concepts dalam automating business processes.

### Tujuan Proyek

- Mengotomatisasi proses bisnis menggunakan n8n workflow platform
- Mengimplementasikan konsep NFA dalam workflow decision logic
- Menyediakan solusi scalable untuk integrasi berbagai aplikasi
- Demonstrasi best practices dalam workflow automation

## ✨ Fitur Utama

- **🔄 Workflow Automation**: Automasi proses bisnis yang kompleks
- **🔌 Multi-Integration**: Integrasi dengan berbagai platform pihak ketiga
- **📊 Data Processing**: ETL (Extract, Transform, Load) capabilities
- **⚡ Real-time Triggers**: Event-based workflow execution
- **🔐 Security**: Secure credential management dan API key handling
- **📈 Scalability**: Arsitektur yang dapat diskalakan untuk berbagai use case

## 🔧 Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **n8n** (Self-hosted atau Cloud version)
  - Version: 0.200.0 atau lebih tinggi
- **Node.js** 16+ (untuk self-hosted installation)
- **Docker** (opsional, untuk containerized deployment)
- **Git** untuk version control
- Text editor atau IDE (VS Code recommended)

### Instalasi n8n

**Menggunakan Docker (Recommended):**
```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

**Menggunakan npm:**
```bash
npm install -g n8n
n8n start
```

## 📦 Instalasi

1. **Clone Repository**
   ```bash
   git clone https://github.com/KaffahRizal/Tugas-Akhir_N8n_nfa.git
   cd Tugas-Akhir_N8n_nfa
   ```

2. **Setup n8n Environment**
   ```bash
   # Jika menggunakan self-hosted
   npm install
   ```

3. **Import Workflows**
   - Buka n8n dashboard di `http://localhost:5678`
   - Navigate ke Workflows
   - Import workflow files dari repository
   - Configure credentials dan environment variables

4. **Configure Environment Variables**
   ```bash
   cp .env.example .env
   # Edit .env dengan konfigurasi Anda
   ```

## 🚀 Penggunaan

### Menjalankan Workflow

1. **Akses n8n Dashboard**
   ```
   URL: http://localhost:5678
   ```

2. **Load Workflow**
   - Buka workflow yang diinginkan
   - Klik tombol "Execute Workflow"
   - Monitor execution logs di sidebar

3. **Manual Trigger**
   ```bash
   curl -X POST http://localhost:5678/webhook/workflow-name
   ```

### Contoh Workflow

Workflow dasar meliputi:
- Data collection dari multiple sources
- Transformation dan validation
- Decision logic menggunakan NFA concepts
- Output ke berbagai destinations

## 📁 Struktur Proyek

```
Tugas-Akhir_N8n_nfa/
├── README.md
├── .env.example
├── .gitignore
├── workflows/
│   ├── workflow-1.json
│   ├── workflow-2.json
│   └── ...
├── credentials/
│   ├── api-keys-config.json
│   └── ...
├── docs/
│   ├── workflow-documentation.md
│   ├── architecture.md
│   └── setup-guide.md
└── tests/
    ├── workflow-tests.json
    └── ...
```

## 🔄 Workflow Details

### Workflow Architecture

Workflow dibangun dengan komponen-komponen berikut:

1. **Trigger Nodes**: Event atau schedule yang memulai workflow
   - Webhook triggers
   - Schedule triggers
   - Poll triggers

2. **Processing Nodes**: Memproses dan transform data
   - HTTP requests
   - Data transformation
   - Conditional logic (NFA-based)

3. **Action Nodes**: Output dan integrasi
   - Database updates
   - API calls
   - Notification sending

### NFA Implementation

Workflow menggunakan NFA concepts untuk:
- State-based decision making
- Multiple parallel execution paths
- Flexible routing logic

## 🛠️ Configuration

### Environment Variables

```env
# n8n Configuration
N8N_HOST=localhost
N8N_PORT=5678
N8N_PROTOCOL=http

# Database (jika diperlukan)
DB_TYPE=sqlite
DB_SQLITE_PATH=/home/node/.n8n/database.sqlite

# Webhook
WEBHOOK_URL=http://localhost:5678

# External Services
API_KEY=your_api_key_here
API_SECRET=your_api_secret_here
```

## 🧪 Testing

Untuk testing workflow:

```bash
# Import test workflows
# Execute dan verify outputs
# Monitor logs untuk debugging
```

## 📚 Dokumentasi Tambahan

- [n8n Official Documentation](https://docs.n8n.io/)
- [Workflow Documentation](./docs/workflow-documentation.md)
- [Setup Guide](./docs/setup-guide.md)
- [Architecture Guide](./docs/architecture.md)

## 🤝 Kontribusi

Kami menyambut kontribusi! Silakan ikuti langkah berikut:

1. Fork repository ini
2. Buat branch fitur (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buka Pull Request

### Guidelines

- Ikuti existing code style
- Tambahkan dokumentasi untuk fitur baru
- Test workflow sebelum submit PR
- Update README jika diperlukan

## 📄 Lisensi

Project ini dilisensikan di bawah MIT License - lihat file [LICENSE](LICENSE) untuk detail.

## 👤 Kontak

**Kaffah Rizal**
- GitHub: [@KaffahRizal](https://github.com/KaffahRizal)
- Repository: [Tugas-Akhir_N8n_nfa](https://github.com/KaffahRizal/Tugas-Akhir_N8n_nfa)

## 🎓 Academic Information

- **Tipe**: Tugas Akhir / Capstone Project
- **Platform**: n8n Workflow Automation
- **Focus Area**: NFA (Non-deterministic Finite Automaton) Integration
- **Status**: Active Development

## 📌 Useful Resources

- [n8n Community](https://community.n8n.io/)
- [n8n Nodes Documentation](https://docs.n8n.io/nodes/)
- [Workflow Best Practices](https://docs.n8n.io/nodes/best-practices/)

---

<div align="center">

Made with ❤️ by Kaffah Rizal

</div>
