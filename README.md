# 🛠️  Utility Library

A general-purpose C++ utility class that provides a collection of static helper methods for random generation, encryption, array manipulation, and more.

---

## 📖 Overview

`clsUtil` is a reusable C++ utility class containing static methods that cover common programming tasks. It depends on `clsDate` for date swapping support and is designed to be used across multiple projects as a shared toolkit.

---

## ✨ Features

- **Random Number Generation**: Generate random integers within a specified range
- **Random Character & Word Generation**: Generate random characters, words, or license-style keys by character type
- **Key Generator**: Generate formatted keys in `XXXX-XXXX-XXXX-XXXX` style
- **Array Filling**: Fill arrays with random numbers, words, or keys
- **Array Shuffling**: Shuffle integer or string arrays randomly
- **Generic Swap**: Swap values of any type (int, double, bool, char, string, clsDate)
- **Text Encryption/Decryption**: Simple Caesar cipher-based encryption and decryption
- **Tab Utility**: Generate a string of tab characters for formatted output

---

## 🚀 How to Use

Include the header file in your project:

```cpp
#include "clsUtil.h"
```

### Random Generation
```cpp
clsUtil::Srand(); // Call once at program start

int num = clsUtil::RandomNumber(1, 100);  // Random int between 1 and 100

char c = clsUtil::GetRandomCharacter(clsUtil::CapitalLetter);  // Random A-Z

string word = clsUtil::GenerateWord(clsUtil::Digit, 6);  // e.g. "482931"

string key = clsUtil::GenerateKey(clsUtil::MixChars);  // e.g. "aB3x-Kd9Z-..."

clsUtil::GenerateKeys(5, clsUtil::CapitalLetter);  // Print 5 keys
```

### Swap & Shuffle
```cpp
int a = 5, b = 10;
clsUtil::Swap(a, b);  // a=10, b=5

int arr[100] = {1, 2, 3, 4, 5};
clsUtil::ShuffleArray(arr, 5);
```

### Encryption
```cpp
string encrypted = clsUtil::EncryptText("Hello", 3);  // "Khoor"
string decrypted = clsUtil::DecryptText(encrypted, 3); // "Hello"
```

---

## 🧠 Concepts Used

- **OOP** — All methods encapsulated as static members inside a class
- **Static Methods** — Callable without creating an instance
- **Enums** — `enCharType` for readable character type selection (Small, Capital, Digit, Mix, Special)
- **Method Overloading** — `Swap()` supports int, double, bool, char, string, and clsDate
- **Random Number Generation** — Uses `rand()` and `srand()` with time seeding
- **Caesar Cipher** — Simple character shifting for encryption and decryption
- **Pass by Reference** — Used in `Swap()` and `ShuffleArray()` for in-place modification
- **Loops** — Used in word generation, array filling, shuffling, and key generation
- **Dependency** — Uses `clsDate` for date swap support

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `Srand()` | Seeds the random number generator (call once at startup) |
| `RandomNumber()` | Generates a random integer between From and To |
| `GetRandomCharacter()` | Returns a random character based on the specified type |
| `GenerateWord()` | Generates a random word of a given length and character type |
| `GenerateKey()` | Generates a formatted `XXXX-XXXX-XXXX-XXXX` key |
| `GenerateKeys()` | Prints multiple generated keys to the console |
| `FillArrayWithRandomNumbers()` | Fills an int array with random numbers |
| `FillArrayWithRandomWords()` | Fills a string array with random words |
| `FillArrayWithRandomKeys()` | Fills a string array with random keys |
| `Swap()` | Swaps two values of any supported type |
| `ShuffleArray()` | Randomly shuffles an int or string array |
| `EncryptText()` | Encrypts a string using a Caesar cipher key |
| `DecryptText()` | Decrypts a string using a Caesar cipher key |
| `Tabs()` | Returns a string of tab characters for formatted output |

---

## 📄 License

This project is open source and free to use for educational purposes.

---

## 👤 Author

👤 **Mahmoud Abd El-Sattar**  
📧 mahmoud.abdelsattar.dev@gmail.com  
💼 [linkedin.com/in/mahmoud-abd-el-sattar](https://www.linkedin.com/in/mahmoud-abd-el-sattar-1b227522a)
