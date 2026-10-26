# Lab-Exercise---3---Hill-Cipher

## Aim :
To develop a simple C program to implement Hill 

## Procedure :

1. Start the program and enter the plaintext.
2. Enter the key matrix for the Hill cipher.
3. Convert the plaintext letters into numerical values (A = 0, B = 1, …, Z = 25).
4. Divide the plaintext into blocks and multiply each block by the key matrix modulo 26.
5. Convert the resulting numerical values back into letters to obtain the encrypted text.
6. Display the encrypted message and test the algorithm with different key values.

## Program :
```
key = [[3, 3],
       [2, 5]]

plaintext = input("Enter plaintext: ").upper().replace(" ", "")

# Add X if the plaintext length is odd
if len(plaintext) % 2 != 0:
    plaintext += "X"

ciphertext = ""

for i in range(0, len(plaintext), 2):
    a = ord(plaintext[i]) - ord('A')
    b = ord(plaintext[i + 1]) - ord('A')

    c1 = (3 * a + 3 * b) % 26
    c2 = (2 * a + 5 * b) % 26

    ciphertext += chr(c1 + ord('A'))
    ciphertext += chr(c2 + ord('A'))

print("Plaintext:", plaintext)
print("Ciphertext:", ciphertext)
```

## Output :
<img width="1492" height="1011" alt="image" src="https://github.com/user-attachments/assets/9dbb1ffe-a23c-4221-98de-c4a6cbf8c71a" />


## Result :
Thus, the program is executed successfully.

