Other Cheat Sheets
==================

## Using `less` instead of tail

```shell
less +F -R /path/to/logfile.log
```

* To scroll up and down, press `<ctrl>+c`
* Return to tail mode, press `F`

The `+F` says to follow? The `-R` will process any ANSII color codes.
