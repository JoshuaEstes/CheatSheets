GnuPG Cheat Sheet
=================

## Listing Key Pairs

```bash
gpg --list-keys
```

For listing keys with the fingerprint, run

```bash
gpg --fingerprint
```

## Generate New Key Pair

```bash
gpg --gen-key
```

## Encrypt a message on command line

```bash
echo "Put message here" | gpg --armor --encrypt --recipient Joshua > FILE.gpg
```

This will put the encrypted text into `FILE.gpg` which you can send to someone or keep for
later use. For decrypting the message, see the next section.

## Decrypt a message from the command line

```bash
cat FILE.gpg | gpg
```

Displays the decrypted text on the command line.

## Only display user X's key information

```bash
gpg --fingerprint Joshua
```

## Signing Messages

```bash
echo "This is a top secret message" | gpg --clearsign
```

## Signing Text Files

```bash
gpg --clearsign example.txt
```

This will create `example.txt.asc` file.

## Verify Signatures

```bash
gpg --verifiy example.txt.asc
```

