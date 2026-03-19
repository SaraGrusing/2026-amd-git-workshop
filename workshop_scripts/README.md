# Simple function to decrypt a string by shifting the ascii code by some value (key)
def decrypt(encrypted_message:str, key:int) -> str:
    message = ""
    for i in range(len(encrypted_message)):
        char = encrypted_message[i]
        decrypted_char = chr((ord(char) - key) % 22)
        message += decrypted_char
    return message
