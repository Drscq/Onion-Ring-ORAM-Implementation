# Onion Ring ORAM: Efficient Constant Bandwidth Oblivious RAM from (Leveled) TFHE (Under Construction)

## Overview
Onion Ring ORAM is a cryptographic primitive that allows a client to hide access patterns to its data encrypted and stored on a remote server. This implementation is based on the paper "Onion Ring ORAM: Efficient Constant Bandwidth Oblivious RAM from (Leveled) TFHE". Our goal is to provide an efficient constant bandwidth ORAM scheme using homomorphic encryption.

## Abstract
Oblivious RAM (ORAM) is a cryptographic primitive that allows a client to hide access pattern to its data encrypted and stored at a remote server. Traditionally, ORAM algorithms assume the server acts purely as a storage device. Under this assumption, ORAM has at least log(N ) bandwidth blowup for N data entries. After three decades of improvements, ORAM algorithms have reached the optimal logarithmic bandwidth blowup. Nonetheless, in many practical use cases, a constant bandwidth overhead is desirable. To this purpose, Devadas et al. (TCC 2016) formalized the server computation model for ORAM and proposed Onion ORAM which relies on homomorphic computation to achieve constant worst-case bandwidth blowup. This line of work is generally believed to be purely theoretical, due to the large overheads of homomorphic computation. In this paper, we present Onion Ring ORAM, the first efficient constant bandwidth ORAM scheme in the single server model, based on the Onion ORAM construction and the leveled version of the TFHE scheme by Chillotti et al.. We propose a series of improvements, most notably including a more efficient homomorphic permutation protocol. We implement Onion Ring ORAM and show that it can outperform state-of-the-art logarithmic-bandwidth ORAM like Path ORAMs and Ring ORAM when the network throughput is limited. Under one setting, our construction reduces monetary cost per access by 40% and end-to-end latency by 35% over Ring ORAM.

## Features
- Constant bandwidth overhead
- Efficient homomorphic permutation protocol
- Implementation using leveled TFHE scheme
- Performance improvements over Path ORAMs and Ring ORAM

## Prerequisites
To build and run this project, you will need:
- C++17 or later
- CMake 3.10 or later
- A C++ compiler (GCC, Clang, MSVC, etc.)
- TFHE library

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/OnionRingORAM.git
    cd OnionRingORAM
    ```

2. Install dependencies:
    Follow the instructions for installing the TFHE library from its [official repository](https://github.com/tfhe/tfhe).

3. Build the project:
    ```sh
    mkdir build
    cd build
    cmake ..
    make
    ```

## Usage
Provide a brief example of how to use the implementation:

```cpp
#include "OnionRingORAM.h"

int main() {
    // Initialize the ORAM
    OnionRingORAM oram;

    // Perform read and write operations
    auto data = oram.read(address);
    oram.write(address, new_data);

    return 0;
}
```

## Documentation
Detailed documentation can be found in the `docs/` directory. The documentation includes a comprehensive guide on how to use the library, including API references and examples.

## Contributing
We welcome contributions! Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## Contact
For any inquiries or questions, feel free to open an issue or contact the project maintainers at `changqi@vt.edu`.