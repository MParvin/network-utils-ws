# 📘 Network Utilities Service — README

A modular FastAPI service providing network‑level diagnostic tools:

- **TLS certificate checks**  
- **HSTS validation**  
- **HTTP→HTTPS redirect analysis**  
- **DNS queries**  
- **WHOIS lookups**  
- **DNSSEC validation**  
- **Reverse DNS**  
- **SOA + AXFR tests**  

The service exposes clean JSON APIs suitable for automation, monitoring, and security auditing.

## 🚀 Features

- **Certificate inspection** (expiry, SAN, issuer, subject)  
- **HSTS header parsing** (max‑age, preload, includeSubDomains)  
- **Redirect chain tracing**  
- **DNS record proxy** (A, AAAA, MX, TXT, etc.)  
- **WHOIS raw + parsed output**  
- **DNSSEC RRSET validation**  
- **Reverse DNS (PTR)**  
- **SOA + AXFR zone transfer test**  
- **Built‑in `/health` endpoint** for container orchestration  

## **Running in Docker**

Pull latest image:

```
docker pull sharevb/network-utils-ws:latest
```

Run it with access to the host Docker daemon:

```
docker run \
  -p 8000:8000 \
  sharevb/network-utils-ws:latest
```

## 🧰 Development

Install dependencies:

```bash
pip install -r requirements.txt
```

Run locally:

```bash
uvicorn main:app --reload
```

## 📄 License

MIT