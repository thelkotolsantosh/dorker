A comprehensive command-line security research tool for penetration testing, bug bounty hunting, and reconnaissance. This toolkit combines Google dorking, email enumeration, directory busting, and vulnerability scanning into one powerful CLI.

⚠️ Legal Disclaimer
This tool is for authorized security testing and educational purposes only.

✅ Only use on systems you own or have explicit permission to test
✅ Follow responsible disclosure practices
✅ Respect bug bounty program rules and scope
✅ Comply with all applicable laws and regulations
❌ Unauthorized access to systems is illegal

The authors are not responsible for misuse or damage caused by this tool.
✨ Features
🔍 Google Dorking

Domain enumeration and subdomain discovery
Bug bounty program finder
Sensitive file detection
Hall of fame and rewards tracking
Custom dork templates

📧 Email Enumeration

Automated email discovery via Google search
Domain-specific email extraction
Pattern-based email validation
Export to text file

📂 Directory Busting

Common directory and file discovery
Custom wordlist support
Status code reporting
Response size analysis

🔐 Vulnerability Scanner

Security headers analysis
Common vulnerability checks
Open redirect detection
JSON report generation

🚀 Installation
Prerequisites

Python 3.6 or higher
pip (Python package manager)

Quick Install
bash# Clone the repository
git clone https://github.com/thelkotolsantosh/dorker.git
cd security-toolkit-cli

# Install required dependencies
pip install -r requirements.txt

# Make the script executable (Linux/Mac)
chmod +x dorker.py
Optional: Google Custom Search API Setup
For better dorking results (recommended):

Get a Google API Key: https://developers.google.com/custom-search/v1/overview
Create a Custom Search Engine: https://programmablesearchengine.google.com/
Set environment variables:

bashexport GOOGLE_API_KEY="your-api-key-here"
export GOOGLE_CX="your-custom-search-engine-id"
Note: Without API keys, the tool will use the fallback googlesearch module (less reliable, rate-limited).
📖 Usage
Interactive Mode (Recommended for Beginners)
Simply run the script without arguments:
bashpython3 dorker.py
Follow the interactive prompts to:

Enter target domain
Choose module (Dorking, Email Enum, DirBust, VulnScan)
View and save results

Command-Line Mode (Advanced)
bash# Google Dorking
python3 dorker.py --target example.com --module dork --dork-type 1

# Email Enumeration
python3 dorker.py --target example.com --module email --output emails.txt

# Directory Busting
python3 dorker.py --target https://example.com --module dirbust

# Directory Busting with Custom Wordlist
python3 dorker.py --target https://example.com --module dirbust --wordlist custom.txt

# Vulnerability Scan
python3 dorker.py --target https://example.com --module vulnscan

# Full Scan (All Modules)
python3 dorker.py --target example.com --module full
Dork Categories

Domain Enumeration - Subdomains, dev environments, staging servers
Bug Bounty Reconnaissance - Security pages, disclosure policies, bounty programs
Rewards/Hall of Fame - Acknowledged researchers, bounty awards
Sensitive Files - Config files, backups, credentials
All Dorks - Run all categories

📋 Command-Line Options
  --target, -t        Target domain or URL (e.g., example.com)
  --module, -m        Module to run (dork/email/dirbust/vulnscan/full)
  --dork-type         Dork category (1-5)
  --output, -o        Output file path
  --wordlist, -w      Custom wordlist for directory busting
📁 Output Files
The tool generates timestamped output files:

dork_results_YYYYMMDD_HHMMSS.csv - Dorking results with links and snippets
emails_YYYYMMDD_HHMMSS.txt - Discovered email addresses
directories_YYYYMMDD_HHMMSS.txt - Found directories with status codes
vulnscan_YYYYMMDD_HHMMSS.json - Vulnerability scan report

🔧 Configuration
Custom Dork Templates
Edit the dork lists in dorker.py:
pythonDOMAIN_ENUM_DORKS = [
    "site:*.example.com -www",
    "your custom dork here",
]
Custom Directory Wordlist
Create a text file with one directory per line:
admin
login
dashboard
api/v1
Then use with --wordlist custom.txt

📚 Examples
Example 1: Bug Bounty Reconnaissance
bashpython3 dorker.py
# Enter: tesla.com
# Choose: 1 (Google Dorking)
# Choose: 2 (Bug Bounty Recon)
Example 2: Full Domain Assessment
bashpython3 dorker.py --target example.com --module full
Example 3: Directory Enumeration with Custom Wordlist
bashpython3 dorker.py -t https://example.com -m dirbust -w wordlists/big.txt

🐛 Troubleshooting
"No search method available"
Install googlesearch module: pip install googlesearch-python
Or set up Google API keys (recommended)
Rate Limiting / IP Blocks
Use Google Custom Search API instead of scraping
Add delays between requests (already implemented)
Use proxy or VPN if needed
Permission Denied
Make script executable: chmod +x dorker.py
Run with python3: python3 dorker.py

🤝 Contributing
Contributions are welcome! Please:
Fork the repository
Create a feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
Ideas for Contributions
Additional vulnerability checks
More dork templates
Integration with other APIs (Shodan, Censys)
Export formats (HTML, PDF)
Multi-threading support
Subdomain takeover detection

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
Google Custom Search API
OWASP for security testing guidelines
Bug bounty platforms (HackerOne, Bugcrowd, etc.)
The security research community

📞 Support
🐛 Report bugs: GitHub Issues
💬 Discussions: GitHub Discussions
 Contact: thelkotolsantosh@gmail.com

⭐ Star History
If you find this tool useful, please give it a star! ⭐
🔐 Security
If you discover a security vulnerability in this tool, please report it responsibly thelkotolsantosh@gmail.com
