OpenSSL Cheat Sheet
===================

## Generate Self-Signed Certificate and Private Key

```shell
openssl genrsa -des3 -passout pass:x -out server.pass.key 2048 && openssl rsa -passin pass:x -in server.pass.key -out server.key && openssl req -new -key server.key -out server.csr
openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt
```

- Use `server.crt` and `server.key`

### Encypt/Decrypt file

```
# Encrypt
openssl aes-128-cbc -a -e -pass pass:test -in vars -out vars.enc
# Puts encrypted data into vars.enc file

# Decrypt
openssl aes-128-cbc -a -d -pass pass:test -in vars.enc
# Outputs decrypted data to STDOUT
```

NOTE: See `openssl passpharse arguments` for information on using the password on the commandline. It can be changed to a file or an environment variable.
