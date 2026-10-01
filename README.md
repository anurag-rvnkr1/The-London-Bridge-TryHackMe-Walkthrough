# The London Bridge — TryHackMe Walkthrough

A professional, portfolio-oriented security write-up for the **TryHackMe — The London Bridge** room.

## What this repository demonstrates

- Network and service enumeration with **Nmap**
- Web application mapping and content discovery
- Request interception with **Burp Suite**
- Parameter fuzzing with **FFUF**
- Directory enumeration with **Feroxbuster**
- **Server-Side Request Forgery (SSRF)** identification and validation
- Loopback filtering bypass analysis
- Internal web-service enumeration through SSRF
- SSH initial access using recovered key material
- Linux host enumeration with **linPEAS**
- Kernel-level privilege-escalation validation
- Offline Firefox profile credential recovery
- Professional evidence handling and secret redaction

## Repository layout

```text
.
├── Documentation/
│   ├── Documentation.md
│   └── documentation.doc
├── Resources/
│   └── notes.md
├── Screenshots/
├── docs/
│   ├── _config.yml
│   ├── _includes/head-custom.html
│   ├── index.md
│   └── assets/
│       ├── css/custom.scss
│       └── *.png
├── .github/workflows/pages.yml
├── SECURITY.md
├── CREDITS.md
├── _config.yml
└── README.md
```

## Public-copy policy

Flags, passwords, private-key contents, and other reusable secrets are deliberately **redacted**. The goal is to demonstrate methodology, validation, and security reasoning without publishing challenge answers.

The screenshot set in `docs/assets/` contains **original lab-style recreations** based on the documented workflow; it is not a redistribution of the reference article's screenshots.

## Documentation

- [Full Markdown write-up](Documentation/Documentation.md)
- [GitHub Pages version](docs/index.md)
- [Research notes](Resources/notes.md)
- [Credits & attribution](CREDITS.md)
- [Security policy](SECURITY.md)

## Reference

Tommaso Greco, *The London Bridge — TryHackMe*, Medium, December 16, 2024.

https://medium.com/@tommasogreco/the-london-bridge-tryhackme-2c8f2f0e5b5a

## Disclaimer

This content is for authorized security-learning environments such as TryHackMe. Never test systems that you do not own or do not have explicit permission to assess.
