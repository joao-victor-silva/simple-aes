# AES cipher

## Usage

### ECB encrypt

To encrypt a binary file you need to inform the input file path that you want to encrypt (`-f`),
the key file path to use during the encryption (`-k`) and the output file path (`-o`). Example

```bash
./main.py cipher -k ecb/key.bin -f ecb/plain.bin -o ciphered.bin
```


### ECB encrypt

To decrypt a binary file you need to inform the input file path that you want to decrypt (`-f`),
the key file path to use during the decryption (`-k`) and the output file path (`-o`). Example

```bash
./main.py decipher -k ecb/key.bin -f ciphered.bin -o deciphered.bin
```


### CTR (encryption and decryption)

To encrypt or decrypt a binary file using CTR mode, you need to inform the input file path (`-f`),
the key file path to use (`-k`) and the output file path (`-o`). You can also inform the initialization vector to be incremented (`-i`), if not informed will be used a vector of `0x00` with 16 elements. Example:

```bash
./main.py ctr -k ctr/key.bin -f ctr/plain.bin -i ctr/iv.bin -o ciphered.bin
```

```bash
./main.py ctr -k ctr/key.bin -f ciphered.bin -i ctr/iv.bin -o deciphered.bin
```
