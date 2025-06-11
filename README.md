# caesar-decrypt-task.py
<pre>
`python Python project to decrypt Caesar
def caesar_decrypt(cipher_text, key):
    result = ""
    for char in cipher_text:
        if char.isalpha(): 
            shift = key % 26
            if char.islower():
                result += chr((ord(char) - ord('a') - shift) % 26 + ord('a'))
            elif char.isupper():
                result += chr((ord(char) - ord('A') - shift) % 26 + ord('A'))
        else:
            result += char  
    return result
cipher_text = "Wklv lv d whvw phvvdjh"

print(":")
for key in range(1, 26): 
    decrypted = caesar_decrypt(cipher_text, key)
    print(f" {key}: {decrypted}")
