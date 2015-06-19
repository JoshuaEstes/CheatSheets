OpenSSL Cheat Sheet
===================

## Generate Self-Signed Certificate and Private Key

```bash
openssl req -newkey rsa:2048 -nodes -keyout server.key -x509 -days 365 -out server.crt
```
