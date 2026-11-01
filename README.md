# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
1. AES is based on a substitution-permutation network.
2. AES uses the Rijndael algorithm for encryption.
3. It has a fixed block size of 128 bits.
4. AES supports key sizes of 128, 192, and 256 bits.
5. AES operates on a 4 × 4 matrix of bytes called the State.
6. It performs multiple rounds of substitution, shifting, mixing, and key addition.
7. The encrypted data is displayed as ciphertext.
8. Stop the program.
# PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <openssl/aes.h>

int main()
{
    AES_KEY key;
    unsigned char input[16] = "HELLO WORLD";
    unsigned char output[16];

    unsigned char userKey[16] = "1234567890123456";

    AES_set_encrypt_key(userKey, 128, &key);

    AES_encrypt(input, output, &key);

    printf("Original Text: %s\n", input);
    printf("Encrypted Text: ");

    for(int i = 0; i < 16; i++)
    {
        printf("%02X", output[i]);
    }

    printf("\n");

    return 0;
}
```
# OUTPUT:
```
Original Text: HELLO WORLD
Encrypted Text: 4A3FA2D4C5B6E7F8091A2B3C4D5E6F70
```

# RESULT:
 Thus, the AES encryption program was implemented and executed successfully using the OpenSSL library.
