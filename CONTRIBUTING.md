# Contributing to Enhanced Crypto Mnemonic Hunter Pro

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## 🤝 Ways to Contribute

### 1. Report Bugs
- Use GitHub Issues
- Include Python version, OS, and error messages
- Provide steps to reproduce
- Include relevant logs/screenshots

### 2. Suggest Features
- Open a GitHub Discussion first
- Explain the use case
- Consider backward compatibility
- Be open to feedback

### 3. Submit Code
- Fork the repository
- Create a feature branch
- Follow coding standards
- Submit a Pull Request

### 4. Improve Documentation
- Fix typos
- Add examples
- Clarify confusing sections
- Translate to other languages

### 5. Test & Report
- Test edge cases
- Report performance issues
- Verify on different platforms
- Share optimization findings

---

## 🔧 Development Setup

### Prerequisites
```bash
Python 3.8+
pip
git
```

### Setup Steps

1. **Fork & Clone**
```bash
git clone https://github.com/YOUR_USERNAME/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO.git
cd ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO
```

2. **Create Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
pip install -r requirements-dev.txt  # If available
```

4. **Create Branch**
```bash
git checkout -b feature/your-feature-name
```

---

## 📝 Coding Standards

### Python Style Guide
- Follow PEP 8
- Use meaningful variable names
- Add docstrings to functions
- Keep functions focused and small
- Maximum line length: 100 characters

### Example
```python
def check_api(self, address, coin_config):
    """
    Check balance and transactions via API.
    
    Args:
        address (str): Wallet address to check
        coin_config (dict): Configuration for the coin
        
    Returns:
        tuple: (balance, transaction_count)
    """
    # Implementation
    pass
```

### Code Organization
```
├── Core logic
│   ├── Mnemonic generation
│   ├── Address derivation
│   └── API checking
├── UI components
│   ├── Main window setup
│   ├── Control widgets
│   └── Console output
└── Utility functions
    ├── File operations
    ├── Logging
    └── Configuration
```

---

## 🧪 Testing

### Before Submitting
- [ ] Run in test mode successfully
- [ ] Test with different configurations
- [ ] Verify on multiple coins
- [ ] Check for memory leaks
- [ ] Test error handling
- [ ] Verify file outputs

### Manual Testing Checklist
```python
# Test configurations
1. Single path + single thread
2. Multi-path + parallel threads
3. Test mode (100 samples)
4. Different word counts (12/24)
5. Different coins (ETH, BTC, etc.)
6. Error scenarios (invalid API, network issues)
```

---

## 📤 Pull Request Process

### 1. Before Creating PR
- Update to latest main branch
- Resolve any conflicts
- Test thoroughly
- Update documentation if needed

### 2. PR Description Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Performance improvement
- [ ] Documentation update

## Testing
- [ ] Tested locally
- [ ] Test mode passed
- [ ] Different configurations tested

## Screenshots (if UI changes)
[Add screenshots here]

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] No breaking changes (or documented)
```

### 3. Review Process
- Maintainer will review within 1-7 days
- Address feedback promptly
- Be open to suggestions
- Update PR as needed

---

## 🐛 Bug Report Template

```markdown
### Bug Description
Clear description of the bug

### Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. See error

### Expected Behavior
What should happen

### Actual Behavior
What actually happens

### Environment
- OS: [e.g., Windows 10]
- Python Version: [e.g., 3.9.7]
- App Version: [e.g., 6.0]

### Error Messages
```
Paste error messages here
```

### Screenshots
If applicable, add screenshots

### Additional Context
Any other relevant information
```

---

## 💡 Feature Request Template

```markdown
### Feature Description
Clear description of the feature

### Problem It Solves
What problem does this address?

### Proposed Solution
How would this work?

### Alternatives Considered
What other options did you consider?

### Additional Context
Screenshots, mockups, examples
```

---

## 🏗️ Architecture Guide

### Main Components

#### 1. MnemonicHunterEnhanced Class
```python
- __init__(): Initialize UI and variables
- setup_ui(): Create interface
- main_loop(): Core scanning logic
- check_api(): API interaction
- derive_address(): BIP44 derivation
```

#### 2. Threading Model
```python
- Main Thread: UI updates
- Worker Threads: API checking
- Thread Pool: Concurrent operations
- Queue: Inter-thread communication
```

#### 3. API Integration
```python
- Etherscan family (ETH, BSC, Polygon, etc.)
- BlockCypher (BTC, LTC, DOGE)
- RPC endpoints (SOL, TRX)
```

---

## 📚 Adding New Features

### Adding a New Blockchain

1. **Update coin_config**
```python
def get_coin_config(self, coin_symbol):
    config = {
        # ... existing configs
        "NEW_COIN": {
            "type": "etherscan",  # or blockcypher, rpc
            "coin": Bip44Coins.NEW_COIN,
            "api_key": NEW_COIN_API_KEY,
            "base_url": "https://api.newcoin.com/api",
            "divisor": 10**18
        }
    }
```

2. **Add API key constant**
```python
NEW_COIN_API_KEY = "YOUR_API_KEY"
```

3. **Update UI coin list**
```python
coins_list = [
    "BTC", "ETH", ..., "NEW_COIN"
]
```

4. **Test thoroughly**
```bash
- Test mode
- Real API calls
- Multi-path derivation
- Error handling
```

5. **Update documentation**
- README.md
- OPTIMIZATION_GUIDE.md
- Add to supported coins table

---

## 🔐 Security Considerations

### When Contributing
- Never commit API keys
- Don't include wallet seeds
- Sanitize logs
- Review sensitive data handling
- Test error messages (no leaks)

### Best Practices
```python
# Good
API_KEY = "YOUR_API_KEY"  # Placeholder

# Bad
API_KEY = "sk_live_abc123..."  # Real key
```

---

## 📖 Documentation Guidelines

### Code Comments
```python
# Good
# Check if wallet has balance > 0

# Bad
# This checks the thing
```

### Docstrings
```python
def function_name(param1, param2):
    """
    Brief description.
    
    Detailed explanation if needed.
    
    Args:
        param1 (type): Description
        param2 (type): Description
        
    Returns:
        type: Description
        
    Raises:
        ExceptionType: When and why
    """
```

---

## 🎯 Priority Areas

### High Priority
1. Bug fixes
2. Performance improvements
3. Security enhancements
4. Critical features

### Medium Priority
1. New blockchain support
2. UI improvements
3. Documentation
4. Code refactoring

### Low Priority
1. Nice-to-have features
2. Minor optimizations
3. Code style fixes

---

## 🤔 Questions?

- **General**: Open a Discussion
- **Bugs**: Create an Issue
- **Security**: Email privately (if sensitive)
- **Features**: Start with Discussion

---

## 📜 Code of Conduct

### Our Pledge
- Be respectful and inclusive
- Accept constructive criticism
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior
- Harassment or discrimination
- Trolling or insulting comments
- Publishing others' private information
- Unethical use promotion

---

## 🙏 Recognition

Contributors will be:
- Listed in README.md
- Mentioned in release notes
- Credited in CHANGELOG.md

Thank you for contributing! 🎉

---

**Questions about contributing?**  
Open a Discussion: https://github.com/syabiz/ENHANCED-CRYPTO-MNEMONIC-HUNTER-PRO/discussions
