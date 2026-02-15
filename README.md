# 🚀 ENHANCED CRYPTO MNEMONIC HUNTER PRO v6.0

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey.svg)]()

**Advanced Multi-Chain Cryptocurrency Wallet Recovery & Research Tool**

A powerful, user-friendly desktop application for scanning BIP39 mnemonic phrases across 14 different blockchain networks with multi-path derivation support.

![Screenshot](https://via.placeholder.com/800x500/0a0a0a/00ffcc?text=Enhanced+Mnemonic+Hunter+v6.0)

---

## ⚡ Key Features

### 🎯 Core Capabilities
- ✅ **14 Blockchain Networks** - ETH, BTC, BNB, POLYGON, ARBITRUM, OPTIMISM, AVALANCHE, FANTOM, BASE, SOL, TRX, LTC, BCH, DOGE
- ✅ **Multi-Path Derivation** - Scan up to 20 derivation paths per mnemonic (m/44'/coin'/0'/0/0-19)
- ✅ **Parallel Processing** - Multi-threaded API checking (1-10 concurrent threads)
- ✅ **Smart Rate Limiting** - Automatic API throttling to avoid rate limits
- ✅ **Real-Time Monitoring** - Live speed metrics, runtime tracking, and statistics

### 🚀 Performance
- **30-50 checks/second** (vs 5-10 in standard versions)
- **Configurable parallelism** - Adjust based on your API limits
- **Memory optimized** - Smart logging and resource management
- **24/7 stable** - Designed for long-running operations

### 🎨 User Interface
- Modern dark theme with color-coded results
- Real-time console output with auto-scrolling
- Progress tracking and performance metrics
- Easy-to-use controls with preset configurations

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Quick Start

1. **Clone the repository:**
```bash
git clone https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO.git
cd ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Configure API Keys:**

Edit `mnemonic_hunter_enhanced.py` and add your API keys:

```python
# Get FREE API keys from:
ETH_API_KEY = "your_etherscan_key"        # https://etherscan.io/myapikey
BSC_API_KEY = "your_bscscan_key"          # https://bscscan.com/myapikey
POLY_API_KEY = "your_polygonscan_key"     # https://polygonscan.com/myapikey
ARBITRUM_API_KEY = "your_arbiscan_key"    # https://arbiscan.io/myapikey
OPTIMISM_API_KEY = "your_optimism_key"    # https://optimistic.etherscan.io/myapikey
FANTOM_API_KEY = "your_ftmscan_key"       # https://ftmscan.com/myapikey
AVALANCHE_API_KEY = "your_snowtrace_key"  # https://snowtrace.io/myapikey
```

4. **Run the application:**
```bash
python mnemonic_hunter_enhanced.py
```

---

## 🎮 Usage Guide

### Basic Operation

1. **Select Blockchain** - Choose from 14 supported networks
2. **Set Word Count** - 12 or 24-word mnemonics
3. **Configure Path Range** - Default: 0-9 (MetaMask/TrustWallet standard)
4. **Adjust Threads** - Start with 3-5 for free API tiers
5. **Enable Features:**
   - Multi-Path Scan (recommended)
   - Parallel Checking (for speed)
   - Test Mode (for generating samples)
6. **Click START** - Monitor real-time results

### Configuration Examples

#### 🔰 Beginner (Conservative)
```
Coin: ETH
Words: 12
Path: 0-4
Threads: 3
Multi-Path: ON
Parallel: ON
```

#### ⚡ Recommended (Balanced)
```
Coin: ETH/BNB/POLYGON
Words: 12
Path: 0-9
Threads: 5
Multi-Path: ON
Parallel: ON
```

#### 🔥 Advanced (Maximum Speed)
```
Coin: ETH
Words: 12
Path: 0-19
Threads: 10
Multi-Path: ON
Parallel: ON
```

---

## 🌐 Supported Blockchains

| Blockchain | Symbol | API Type | Derivation Path |
|------------|--------|----------|-----------------|
| Bitcoin | BTC | BlockCypher | m/44'/0'/0'/0/x |
| Ethereum | ETH | Etherscan | m/44'/60'/0'/0/x |
| BNB Chain | BNB | BSCScan | m/44'/714'/0'/0/x |
| Polygon | MATIC | PolygonScan | m/44'/60'/0'/0/x |
| Arbitrum | ARB | Arbiscan | m/44'/60'/0'/0/x |
| Optimism | OP | Optimistic | m/44'/60'/0'/0/x |
| Avalanche | AVAX | Snowtrace | m/44'/60'/0'/0/x |
| Fantom | FTM | FTMScan | m/44'/60'/0'/0/x |
| Base | BASE | BaseScan | m/44'/60'/0'/0/x |
| Solana | SOL | RPC | m/44'/501'/0'/0' |
| Tron | TRX | TronGrid | m/44'/195'/0'/0/x |
| Litecoin | LTC | BlockCypher | m/44'/2'/0'/0/x |
| Bitcoin Cash | BCH | BlockCypher | m/44'/145'/0'/0/x |
| Dogecoin | DOGE | BlockCypher | m/44'/3'/0'/0/x |

---

## 📊 Performance Metrics

### Speed Comparison

| Configuration | Version 5.0 | Version 6.0 | Improvement |
|---------------|-------------|-------------|-------------|
| Single Path | 5-10/s | 15-20/s | **2-3x faster** |
| Multi-Path (10) | N/A | 30-50/s | **New feature** |
| Max Threads | Single | 10 parallel | **10x parallelism** |

### Resource Usage
- **CPU**: 30-70% (depends on thread count)
- **Memory**: 50-200 MB
- **Network**: API rate-limited (respects free tiers)

---

## 📁 Output Files

### Saldo_Found.txt
Wallets with balance > 0:
```
2025-02-15 14:30:22 | abandon ability able... | Path:0 | 0x1234...abcd | Balance:0.05 | ETH
```

### Transaksi_Found.txt
Wallets with transaction history:
```
2025-02-15 14:31:45 | another seed phrase... | Path:3 | 0x5678...efgh | TX:12 | BNB
```

### Test_Mnemonic.txt
Test mode samples (when enabled):
```
word1 word2 word3... | Path:0 | 0xabc...123
```

---

## 🛡️ Security & Ethics

### ⚠️ IMPORTANT DISCLAIMER

This tool is designed for:
- ✅ **Wallet Recovery** - Finding your own lost mnemonics
- ✅ **Educational Research** - Learning about BIP39/BIP44
- ✅ **Security Testing** - Analyzing entropy and randomness

**NOT for:**
- ❌ Unauthorized access to others' wallets
- ❌ Brute-forcing existing wallets
- ❌ Any illegal activities

### Statistical Reality
```
Total 12-word combinations: 2^128 ≈ 3.4 × 10^38
Active wallets (estimated): ~100 million
Probability of random match: ~1 in 3.4 × 10^30

Finding an active wallet randomly is statistically impossible.
This tool is most useful for recovering YOUR OWN lost seeds.
```

---

## 🔧 Troubleshooting

### Common Issues

**Slow Performance?**
- Reduce thread count (3-5 optimal for free APIs)
- Check internet connection
- Verify API keys are valid
- Disable parallel checking if hitting rate limits

**API Errors?**
- Confirm API keys are correct
- Check rate limits (free tier: 5 req/s)
- Wait if you've hit daily limits
- Consider multiple API keys

**High CPU/Memory?**
- Reduce thread count
- Restart application periodically
- Close other programs
- Check for infinite loops in logs

See [OPTIMIZATION_GUIDE.md](OPTIMIZATION_GUIDE.md) for detailed troubleshooting.

---

## 📚 Documentation

- **[README_ENHANCED.md](README_ENHANCED.md)** - Detailed feature documentation
- **[OPTIMIZATION_GUIDE.md](OPTIMIZATION_GUIDE.md)** - Performance tuning and scenarios
- **[LICENSE](LICENSE)** - MIT License terms

---

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contribution
- Additional blockchain support
- UI improvements
- Performance optimizations
- Bug fixes
- Documentation enhancements

---

## 📈 Roadmap

- [ ] Database storage for results
- [ ] Web interface version
- [ ] Multi-language support
- [ ] Advanced pattern matching
- [ ] Export to CSV/JSON
- [ ] Custom derivation paths
- [ ] API key rotation system
- [ ] Docker containerization

---

## 🙏 Acknowledgments

- **BIP39/BIP44** - Bitcoin Improvement Proposals
- **mnemonic** library - Python BIP39 implementation
- **bip-utils** - Hierarchical Deterministic Wallets
- Community feedback and testing

---

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO/issues)
- **Discussions**: [GitHub Discussions](https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO/discussions)

---

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Remember**: Use responsibly and ethically. This tool is for legitimate recovery and research purposes only.

---

## 🌟 Star History

If you find this project helpful, please consider giving it a ⭐ on GitHub!

[![Star History Chart](https://api.star-history.com/svg?repos=syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO&type=Date)](https://star-history.com/#syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO&Date)

---

**Made with ❤️ for the Crypto Community**

*Last Updated: February 2025 | Version 6.0*
