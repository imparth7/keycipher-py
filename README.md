# KeyCipher

`keycipher` is a Python utility package for encrypting and decrypting text using AES-GCM with a secret key. It provides simple functions to handle secure encryption and decryption.

## Installation

To install the package, use pip:

```bash
pip install keycipher
```

## Usage

Here’s a brief guide on how to use the `keycipher` package.

### Importing the Package

```python
from keycipher import encrypt_data, decrypt_data
```

### Encrypting Data

To encrypt a piece of text, use the `encrypt_data` function. You need to provide the plaintext and a key string.

```python
from keycipher import encrypt_data

key_string = 'your-secret-key'  # Replace with your key
plain_text = 'This is a secret message'  # Replace with your text

encrypted_data = encrypt_data(plain_text, key_string)
print('Encrypted Data:', encrypted_data)
```

### Decrypting Data

To decrypt data, use the `decrypt_data` function. You need to provide the encrypted data and the same key string used for encryption.

```python
from keycipher import decrypt_data

encrypted_data = {
    'iv': '...your IV...',
    'cipherText': '...your cipherText...',
    'tag': '...your tag...'
}  # Replace with your generated encryption object

key_string = 'your-secret-key'  # Replace with your key

decrypted_text = decrypt_data(encrypted_data, key_string)
print('Decrypted Text:', decrypted_text)
```

## API

### `encrypt_data(plain_text, key_string)`

Encrypts the given plaintext using the provided key string.

- **Arguments:**
  - `plain_text` (str): The text to be encrypted.
  - `key_string` (str): The key used for encryption.

- **Returns:** A dictionary containing `iv`, `cipherText`, and `tag`.

### `decrypt_data(encrypted_data, key_string)`

Decrypts the given encrypted data using the provided key string.

- **Arguments:**
  - `encrypted_data` (dict): The encrypted data object, which includes `iv`, `cipherText`, and `tag`.
  - `key_string` (str): The key used for decryption.

- **Returns:** The decrypted text.

## Example

Here’s a complete example showing both encryption and decryption:

```python
from keycipher import encrypt_data, decrypt_data

# Encryption
key_string = 'your-secret-key'
plain_text = 'This is a secret message'
encrypted_data = encrypt_data(plain_text, key_string)
print('Encrypted Data:', encrypted_data)

# Decryption
decrypted_text = decrypt_data(encrypted_data, key_string)
print('Decrypted Text:', decrypted_text)
```

## About the Author

`keycipher` is created by Parth Dudhatra (imParth), a passionate software engineer, developer advocate, and content creator known for his contributions to the tech community. He is passionate about frontend development, Python programming, open-source software, and sharing knowledge with others.

Parth is active on various social media platforms, where he shares insights, tutorials, and tips related to programming, web development, and software engineering. Parth's dedication to sharing his expertise and fostering a supportive environment for developers has earned him recognition and respect within the tech community. Connect with Parth Dudhatra on social media:

- [Portfolio](https://imparth.me)
- [X/Twitter](https://x.com/imparth73)
- [Instagram](https://instagram.com/imparth.dev)
- [GitHub](https://github.com/imparth7)
- [LinkedIn](https://linkedin.com/in/imparth7)
- [Medium](https://imparth7.medium.com)
- [Dev.to](https://dev.to/imparth)

If you have any questions, feedback, or suggestions, feel free to reach out to me on any platform!

## License

This project is licensed under the ISC License.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request on the [GitHub repository](https://github.com/imparth7/keycipher-py).

## Issues

If you encounter any issues, please report them on the [issues page](https://github.com/imparth7/keycipher-py/issues).