# EX - 1 Caesar-Cipher-Program
Caeser Cipher using with different key values

# AIM:

To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm.


## DESIGN STEPS:

### Step 1:

Design of Caeser Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

1.	In Ceaser Cipher each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.
2.	For example, with a left shift of 3, D would be replaced by A, E would become B, and so on.
3.	The encryption can also be represented using modular arithmetic by first transforming the letters into numbers, according to the   
    scheme, A = 0, B = 1, Z = 25.
4.	Encryption of a letter x by a shift n can be described mathematically as,
                       En(x) = (x + n) mod26
5.	Decryption is performed similarly,
                       Dn (x)=(x - n) mod26


## PROGRAM:
```
Developed by: Istin B
Register number: 212223040068
```
```
def caesar_cipher(text, shift, encrypt=True):
    result = ""
    
    for char in text:
        if char.isalpha():
            shift_amount = shift if encrypt else -shift
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base + shift_amount) % 26 + base)
        else:
            result += char
            
    return result

plain_text = "Anna University"
shift_value = 5

encrypted_text = caesar_cipher(plain_text, shift_value)
decrypted_text = caesar_cipher(encrypted_text, shift_value, encrypt=False)

print("Encrypted:", encrypted_text)
print("Decrypted:", decrypted_text)

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/6365d4d9-4e21-4e0d-8c55-f7dc4e18e5b2)





## RESULT:
The program is executed successfully
