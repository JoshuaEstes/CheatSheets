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
