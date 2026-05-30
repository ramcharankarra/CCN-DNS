# CCN-DNS: Advanced DNS Resolver

CCN-DNS is a high-performance, modular DNS resolver built with Python, featuring support for multiple resolution modes, advanced caching backends, and a modern GUI.

## 🚀 Features

- **Multiple Resolution Modes**:
  - **Recursive**: Resolves queries by traversing the DNS hierarchy from root servers.
  - **Forwarding**: Forwards queries to upstream providers like Google DNS (8.8.8.8) or Cloudflare (1.1.1.1).
  - **DNS over HTTPS (DoH)**: Securely resolves queries using Google or Cloudflare DoH endpoints.
- **Advanced Caching**:
  - Pluggable backend support for **Memory**, **MongoDB**, and **PostgreSQL**.
  - Intelligent TTL management.
- **Robust Tools**:
  - **Benchmark CLI**: Compare resolution speeds across different modes and providers.
  - **Local DNS Server**: Run a local DNS proxy on port 5353.
- **Modern UI**:
  - Dynamic GUI built with **Electron** and **Next.js** for real-time monitoring and configuration.

## 🛠 Architecture

The project is structured for high modularity:
- `dns_resolver/`: Core logic for packet parsing, resolution, and transport.
- `gui/`: Web-based dashboard for DNS operations.
- `electron_gui/`: Desktop wrapper for the management console.
- `tests/`: Comprehensive test suite for all resolver components.

## 🏁 Getting Started

### Prerequisites
- Python 3.8+
- MongoDB (optional, for persistent caching)
- Node.js & npm (for GUI)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/ramcharankarra/CCN-DNS.git
   cd CCN-DNS
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Resolver
```bash
python CCN-DNS/benchmark_cli.py
```

