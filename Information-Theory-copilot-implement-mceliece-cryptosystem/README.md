# McEliece Cryptosystem Implementation

This repository contains a complete implementation of the McEliece cryptosystem with two variants:
- **Hamming variant**: Uses (15, 11) Hamming codes
- **BCH variant**: Uses (15, 7) BCH codes

## Installation

First, install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Demos

To run the Hamming variant demo:
```bash
python run_hamming_demo.py
```

To run the BCH variant demo:
```bash
python run_bch_demo.py
```

Both demos will:
1. Generate public and private keys
2. Encrypt a random message
3. Decrypt the ciphertext
4. Verify that decryption recovers the original message

### Running the Benchmark

To compare the performance of both variants:
```bash
python run_benchmark.py
```

The benchmark script measures:
- Key generation time
- Encryption time
- Decryption time
- Ciphertext expansion rate
- Public key size

## Implementation Details

### Hamming Variant
- Uses (15, 11) Hamming codes with 1 error correction capability
- Block-diagonal structure with L blocks
- Adds 1 error per block during encryption

### BCH Variant
- Uses (15, 7) BCH codes with 2 error correction capability
- Block-diagonal structure with L blocks
- Adds 2 errors per block during encryption

## Directory Structure

```
code/
  __init__.py
  utils.py                    # Shared utility functions
  hamming_mceliece/
    __init__.py
    hamming_code.py          # Hamming code implementation
    keygen.py                # Key generation
    encrypt.py               # Encryption
    decrypt.py               # Decryption
  bch_mceliece/
    __init__.py
    bch_code.py             # BCH code implementation
    keygen.py               # Key generation
    encrypt.py              # Encryption
    decrypt.py              # Decryption
run_hamming_demo.py         # Hamming demo script
run_bch_demo.py             # BCH demo script
run_benchmark.py            # Benchmark script
requirements.txt            # Dependencies
```