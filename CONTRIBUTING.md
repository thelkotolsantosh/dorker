# Contributing to Dorker

First off, thank you for considering contributing to this 🎉

## Code of Conduct

By participating in this project, you agree to:
- Be respectful and inclusive
- Use the tool for ethical purposes only
- Help maintain a welcoming environment

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear title** - Describe the issue concisely
- **Steps to reproduce** - List exact steps
- **Expected behavior** - What should happen
- **Actual behavior** - What actually happens
- **Environment** - OS, Python version, etc.
- **Error messages** - Include full stack traces

### Suggesting Features

Feature requests are welcome! Please include:

- **Use case** - Why is this feature needed?
- **Proposed solution** - How should it work?
- **Alternatives** - What alternatives have you considered?

### Pull Requests

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Make your changes
4. Test thoroughly
5. Commit with clear messages (`git commit -m 'Add XYZ feature'`)
6. Push to your fork (`git push origin feature/YourFeature`)
7. Open a Pull Request

## Development Setup

```bash
# Clone your fork
git clone https://github.com/thelkotolsantosh/dorker.git
cd security-toolkit-cli

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run tests
python3 security_toolkit.py --help
```

## Coding Guidelines

### Python Style
- Follow PEP 8
- Use meaningful variable names
- Add docstrings to functions
- Keep functions focused and small

### Example:
```python
def check_security_headers(url: str) -> dict:
    """
    Check if security headers are present.
    
    Args:
        url: Target URL to check
        
    Returns:
        Dictionary with header analysis results
    """
    # Implementation here
    pass
```

### Adding New Modules

To add a new security module:

1. Create the function in `security_toolkit.py`
2. Add it to the main menu
3. Create appropriate output format
4. Update README with usage examples
5. Add any new dependencies to `requirements.txt`

### Adding New Dorks

Add to the appropriate dork list:

```python
NEW_CATEGORY_DORKS = [
    "your dork here example.com",
    "another dork site:example.com",
]
```

## Testing

Before submitting PR:

```bash
# Test all modules
python3 security_toolkit.py -t example.com -m dork --dork-type 1
python3 security_toolkit.py -t example.com -m email
python3 security_toolkit.py -t https://example.com -m dirbust
python3 security_toolkit.py -t https://example.com -m vulnscan

# Test interactive mode
python3 security_toolkit.py
```

## Documentation

Update documentation when:
- Adding new features
- Changing existing functionality
- Adding new dependencies
- Modifying CLI arguments

## Questions?

Feel free to open an issue for questions or reach out via discussions!

---

Thank you for contributing! 🙏
