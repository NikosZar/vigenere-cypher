## Vigenère Cipher Implementation  

## Overview
The Vigenère cipher is a polyalphabetic substitution cipher that improves upon the monoalphabetic Caesar cipher. While the Caesar cipher uses a single shift value, the Vigenère cipher uses a keyword to create multiple shift values, making it significantly more resistant to frequency analysis.

## Assignment
Implement a Vigenère cipher encoder/decoder in Ruby that can handle both encryption and decryption operations.
### Input Requirements
Your program should accept three command-line arguments:
1. Operation type (encrypt or decrypt)
2. The message (string)
3. The keyword (string)  

### Constraints
Message may contain:
- Uppercase letters
- Lowercase letters
- Spaces
- Punctuation
- Keyword should contain:
- Only letters (a-z or A-Z)

### Output Requirements
Your implementation must:
- Preserve the case of the original message
- Preserve spaces and punctuation
- Return the encrypted/decrypted message as a string
  
## Technical Specifications
### Mathematical Foundation
The Vigenère cipher can be expressed mathematically as:    
#### For encryption:
```math
Ci = (Pi + Ki) \bmod 26
```

#### For decryption:
```math
Ci = (Pi - Ki) \bmod 26
```
Where:
- Pi is the position of the plaintext letter (0-25)
- Ki is the position of the keyword letter (0-25)
- Ci is the position of the ciphertext letter (0-25)
  
## Implementation Requirements
1. Input validation
2. Error handling for invalid inputs
3. Modular design (separate encryption/decryption logic)
4. Command Line Usage

   
### Development Hints
1. Consider how to handle a keyword shorter than the message
2. Non-alphabetic characters should remain unchanged
3. The keyword should "skip" over spaces and punctuation
4. Use modular arithmetic for alphabet wraparound

#### Test Cases to Consider
- Messages shorter than keyword
- Messages longer than keyword
- Messages with mixed case
- Messages with spaces and punctuation
- Empty messages
- Single-character messages
- Single-character keywords
  
## Bonus Challenge
Implement a function that attempts to crack a Vigenère-encrypted message without the keyword, using frequency analysis and the Index of Coincidence method.
