# VHosts

```bash
gobuster vhost -u jorge.com -w subdomains-top1million-110000.txt --append-domain
```

# Subdomains

```bash
gobuster dns -do inlanefreight.com -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt --no-error
```

