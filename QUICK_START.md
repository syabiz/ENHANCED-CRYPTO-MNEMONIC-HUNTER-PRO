# 🚀 Quick Start Guide

Get up and running in 5 minutes!

## ⚡ Installation (2 minutes)

### Step 1: Clone Repository
```bash
git clone https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO.git
cd ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

**That's it!** You can now run in TEST MODE without API keys.

---

## 🎮 First Run (TEST MODE)

### Run Without API Keys

```bash
python mnemonic_hunter_enhanced.py
```

1. ✅ Check **TEST MODE** checkbox
2. Select coin: **ETH**
3. Words: **12**
4. Path Range: **0** to **9**
5. Threads: **3**
6. Click **▶ START**

**Result**: Will generate 100 sample mnemonics with 10 addresses each in `Test_Mnemonic.txt`

This verifies your installation works!

---

## 🔑 Get FREE API Keys (3 minutes)

### Essential APIs (Free Tier)

#### 1. Etherscan (for ETH, ARBITRUM, OPTIMISM, BASE)
- Visit: https://etherscan.io/register
- Create account
- Go to: https://etherscan.io/myapikey
- Create new API key
- Copy the key

#### 2. BSCScan (for BNB Chain)
- Visit: https://bscscan.com/register
- Create account  
- Go to: https://bscscan.com/myapikey
- Create new API key
- Copy the key

#### 3. PolygonScan (for POLYGON)
- Visit: https://polygonscan.com/register
- Create account
- Go to: https://polygonscan.com/myapikey
- Create new API key
- Copy the key

### Optional APIs (for more chains)

#### 4. Arbiscan (ARBITRUM)
- https://arbiscan.io/myapikey

#### 5. Snowtrace (AVALANCHE)
- https://snowtrace.io/myapikey

#### 6. FTMScan (FANTOM)
- https://ftmscan.com/myapikey

**Note**: BTC, LTC, DOGE work without API keys (BlockCypher free tier)

---

## 🔧 Configure API Keys (1 minute)

### Edit the Script

Open `mnemonic_hunter_enhanced.py` in any text editor:

**Find this section at the top:**
```python
# --- KONFIGURASI API KEY ---
ETH_API_KEY = "YOUR_API_KEY"
BSC_API_KEY = "YOUR_API_KEY"
POLY_API_KEY = "YOUR_API_KEY"
```

**Replace with your keys:**
```python
# --- KONFIGURASI API KEY ---
ETH_API_KEY = "ABCDEF123456789..."
BSC_API_KEY = "XYZ789456123..."
POLY_API_KEY = "QWE456789123..."
```

**Save the file.**

---

## 🎯 Your First Real Scan

### Recommended Settings for Beginners

1. **Uncheck** TEST MODE
2. **Coin**: ETH (most valuable)
3. **Words**: 12
4. **Path Range**: 0 to 4 (most commonly used)
5. **Threads**: 3 (safe for free tier)
6. **Multi-Path**: ON
7. **Parallel**: ON
8. Click **▶ START**

### What to Expect

**Console Output:**
```
[ETH] 0x1234abcd...xyz | TX: 0 | Bal: 0 | word1 word2 word3...
[ETH] 0x5678efgh...abc | TX: 0 | Bal: 0 | word4 word5 word6...
```

**Speed**: ~20-30 checks per second

**Output Files**:
- `Saldo_Found.txt` - If balance > 0 (very rare!)
- `Transaksi_Found.txt` - If TX count > 0 (rare)

---

## 📊 Understanding the UI

### Top Controls

```
┌─────────────────────────────────────────────────┐
│ Coin: [ETH ▼]  Words: [12▼]  Path: [0] to [9] │
│ Threads: [5▼]  ☑ Multi-Path  ☑ Parallel        │
│ ▶ START  ⏸ PAUSE  ⏹ STOP  ✖ EXIT              │
└─────────────────────────────────────────────────┘
```

### Status Display

```
STATUS: RUNNING...
Checked: 1000 | Found: 0 | TX: 0 | Speed: 35/s
Runtime: 00:05:23
```

### Console Colors

- 🟢 **Green Background**: Wallet with BALANCE! 💰
- 🟡 **Yellow Background**: Wallet with TX HISTORY 📊  
- 🔵 **Cyan Text**: System messages
- 🟠 **Orange Text**: Warnings

---

## ⚙️ Common Configurations

### 🔰 Conservative (Safe for Free APIs)
```
Threads: 3
Path: 0-4
Multi-Path: ON
Parallel: ON
```
**Speed**: ~20/s | **API Usage**: Low

---

### ⚡ Balanced (Recommended)
```
Threads: 5
Path: 0-9  
Multi-Path: ON
Parallel: ON
```
**Speed**: ~35/s | **API Usage**: Medium

---

### 🔥 Aggressive (Need Good APIs)
```
Threads: 10
Path: 0-19
Multi-Path: ON
Parallel: ON
```
**Speed**: ~60/s | **API Usage**: High

---

## 🐛 Troubleshooting

### "Too many requests" or API errors
**Solution**: 
- Reduce threads to 2-3
- Check API keys are valid
- Wait a few minutes (rate limit reset)

### Slow speed (<10/s)
**Solution**:
- Check internet connection
- Verify API keys entered correctly
- Try different coin (BTC, LTC don't need keys)

### App freezes or crashes
**Solution**:
- Reduce threads
- Disable parallel checking
- Restart the app
- Check RAM usage

---

## 📁 Where Are My Results?

### Test Mode
```
Test_Mnemonic.txt
```
Contains generated mnemonics and addresses

### Real Scans
```
Saldo_Found.txt        (wallets with balance)
Transaksi_Found.txt    (wallets with TX history)
```

**Location**: Same folder as the script

---

## 💡 Pro Tips

### Tip 1: Start Small
Don't use max settings immediately. Build up gradually:
1. Test mode first
2. Then 3 threads
3. Then 5 threads
4. Monitor for errors

### Tip 2: Focus on Popular Chains
ETH, BNB, POLYGON have most activity
Start there before trying BTC, DOGE, etc.

### Tip 3: Path Priority
- Paths 0-2: 90% of wallets
- Paths 3-4: 8% of wallets
- Paths 5-9: 2% of wallets
- Paths 10+: <0.1% of wallets

### Tip 4: Monitor Performance
Watch the Speed metric:
- 20-30/s = Good
- 30-50/s = Excellent
- >50/s = Amazing (need good APIs)
- <10/s = Problem (check settings)

### Tip 5: Be Patient
Finding an active wallet randomly is:
- Probability: ~1 in 10^30
- Effectively: Impossible
- Best use: Recovery of YOUR lost seeds

---

## 🎯 Next Steps

1. ✅ **Completed Quick Start** - You're running!
2. 📖 **Read [README_ENHANCED.md](README_ENHANCED.md)** - Detailed features
3. ⚙️ **Check [OPTIMIZATION_GUIDE.md](OPTIMIZATION_GUIDE.md)** - Advanced configs
4. 🌟 **Star the repo** on GitHub if helpful!

---

## 🆘 Need Help?

- **Issues**: https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO/issues
- **Discussions**: https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO/discussions

---

## ⚠️ Important Reminder

This tool is for:
- ✅ Wallet recovery (your own)
- ✅ Educational purposes
- ✅ Security research

NOT for:
- ❌ Unauthorized access
- ❌ Illegal activities

Use responsibly and ethically! 🙏

---

**Happy Scanning!** 🚀

*Need more details? Check the full [README.md](README.md)*
