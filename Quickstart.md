# ⚡ Quick Start Guide
Get up and running with dorker CLI in 5 minutes!

# 1️⃣ Installation (2 minutes)
`bash

# Clone the repository
git clone https://github.com/thelkotolsantosh/dorker.git
cd security-toolkit-cli

# Install dependencies
pip install -r requirements.txt
`

# 2️⃣ Basic Usage (1 minute)

# Interactive Mode (Easiest)
`bash
python3 security_toolkit.py
`

Then follow the prompts:
1. Enter target domain (e.g., `example.com`)
2. Choose module (1-6)
3. View results!

# 3️⃣ Quick Examples (2 minutes)

# Find Bug Bounty Programs
`bash
python3 security_toolkit.py -t tesla.com -m dork --dork-type 2
`

# Enumerate Emails
`bash
python3 security_toolkit.py -t example.com -m email
`

# Bust Directories
`bash
python3 security_toolkit.py -t https://example.com -m dirbust
`

# Scan for Vulnerabilities
`bash
python3 security_toolkit.py -t https://example.com -m vulnscan
`

# Run Everything
`bash
python3 security_toolkit.py -t example.com -m full
`

# 📊 Output Files

Results are automatically saved with timestamps:
- `dork_results_20241207_143022.csv`
- `emails_20241207_143022.txt`
- `directories_20241207_143022.txt`
- `vulnscan_20241207_143022.json`

# 🎯 Pro Tips

1. **Use Google API** for better dorking:
   `bash
   export GOOGLE_API_KEY="your-key"
   export GOOGLE_CX="your-cx-id"
   `

2. **Custom wordlist** for directory busting:
   `bash
   python3 security_toolkit.py -t example.com -m dirbust -w custom.txt
   `

3. **Always get permission** before testing!

# 🆘 Need Help?

- Full documentation: See [README.md](README.md)
- Setup issues: See [SETUP_GUIDE.md](SETUP_GUIDE.md)
- Report bugs: [GitHub Issues] https://github.com/thelkotolsantosh/dorker.git

# ⚖️ Remember

- ✅ Only test authorized targets
- ✅ Follow responsible disclosure
- ✅ Respect rate limits
- ❌ Never use on unauthorized systems

---

**Happy Hunting! 🎯**
