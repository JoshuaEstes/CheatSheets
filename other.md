Other Cheat Sheets
==================

## Using `less` instead of tail

```shell
less +F -R /path/to/logfile.log
```

* To scroll up and down, press `<ctrl>+c`
* Return to tail mode, press `F`

The `+F` says to follow? The `-R` will process any ANSII color codes.

## SSH Config File

```
# ~/.ssh/config
Host test
  HostName testing.example.com
  Port 22222
  User joshua
  IdentityFile ~/.ssh/test.example.com.key
```

Next, all you need to do to ssh into the server is `ssh test` and that's it.

> **NOTE** `HostName` may be an IP Address instead of a domain name

## OpenSSL

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
