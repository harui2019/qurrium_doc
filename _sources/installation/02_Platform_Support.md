# Platform Support

The followings are the OS and hardware architecture we support.

It's basically following [the platform support of qiskit](https://docs.quantum.ibm.com/start/install#operating-system-support).

## Available Python Version

![Available Python Version](https://img.shields.io/badge/Python-3.9_|_3.10_|_3.11_|_3.12-blue?logo=python&logoColor=white) [![Downloads](https://static.pepy.tech/badge/qurrium)](https://pepy.tech/project/qurrium)

Qurry is written in Python 3.9 type hint syntax.
It can't and won't support Python 3.8 and below since they are too old.

## Available Operation System and Processor Architecture

![Available System](https://img.shields.io/badge/Ubuntu-18.04+-purple?logo=Ubuntu&logoColor=white) ![Available System](https://img.shields.io/badge/Ubuntu_on_WSL-18.04+-purple?logo=Ubuntu&logoColor=white)
![Available System](https://img.shields.io/badge/Windows-10_|_11-purple?logo=Windows&logoColor=white) ![Available System](https://img.shields.io/badge/MacOS-11+-purple?logo=Apple&logoColor=white)

We strongly recommend to use Linux based system, due to Python multiprocessing may exist some unknown issue on Windows and the GPU acceleration of `Qiskit`, `qiskit-aer-gpu` only works with Nvidia CUDA on Linux.

## Availability

|                           | macos<br/>x86_64 | macos<br/>universal2 | macos<br/>ARM64 | windows<br/>amd64 | windows<br/>win32 | windows<br/>arm64 | linux<br/>x86_64 | linux<br/>i686  | linux<br/>aarch64 |
| ------------------------- | ---------------- | -------------------- | --------------- | ----------------- | ----------------- | ----------------- | ---------------- | --------------- | ----------------- |
| CPython 3.9 <sup>1</sup>  | ✅               | ✅                   | ✅              | ✅                | ✅                | ✅ <sup>2</sup>   | ✅ <sup>3</sup>  | ✅ <sup>3</sup> | ✅ <sup>3</sup>   |
| CPython 3.10 <sup>1</sup> | ✅               | ✅                   | ✅              | ✅                | ✅                | ✅ <sup>2</sup>   | ✅ <sup>3</sup>  | ✅ <sup>3</sup> | ✅ <sup>3</sup>   |
| CPython 3.11 <sup>1</sup> | ✅               | ✅                   | ✅              | ✅                | ✅                | ✅ <sup>2</sup>   | ✅ <sup>3</sup>  | ✅ <sup>3</sup> | ✅ <sup>3</sup>   |
| CPython 3.12 <sup>1</sup> | ✅               | ✅                   | ✅              | ✅                | ✅                | ✅ <sup>2</sup>   | ✅ <sup>3</sup>  | ✅ <sup>3</sup> | ✅ <sup>3</sup>   |

1. All CPython builds are based on the 3.9+ CPython ABI.
2. Although `windows_arm64` builds are provided, they have not been properly tested, as we do not have access to such a machine for testing.
3. All Linux builds are based on `manylinux2014`, consistent with Qiskit's approach for their Linux builds.

- **All ManyLinux 2014 compatible distro**
  Ubuntu 18.04+ LTS, Rocky Linux, ...

  - on `x86_64` **(recommended)**
  - on `x86_64` Windows 10/11 WSL2 **(recommended)**
  - on `aarch64`
    - Fujitsu Quantum Simulator with `qiskit-qulacs` making `qulacs` as a `qiskit` backend to run.
    - Android Terminal emulator `Termux` with `proto-distro`, so you can run this on your Android device if you know how to do.
      - If you want to try this, I suggest using the devices with sufficient performance CPU like Qualcomm Snapdragon 865 with 10GiB RAM at least.
      - See ["Quantum computing right at your fingertips"](https://www.instagram.com/p/C1-dQWdSFYB/?utm_source=ig_web_button_share_sheet&igsh=MzRlODBiNWFlZA==) :)
      - iSH on iOS/iPadOS can not even handle python environment building although iPad has powerful performance :(

- **Windows 10/11** on `x86_64`, `x86_32`, `ARM64`

- **MacOS 11+**
  - on `arm64 (Apple Silicon)`
  - on `x86_64 (Intel chips)`

## Dependencies

- with required modules:

  - `qiskit`, `qiskit-aer`, `tqdm`, `requests`

- with optional modules:
  - `qiskit-aer-gpu`: The CUDA acceleration only on Linux.
    - `qiskit-aer-gpu-cu11`: Extra support for CUDA11.
  - `qiskit-ibm-runtime`: Access IBM Quantum and `FackBackend`.
  - `qiskit-ibm-provider`: Access IBM Quantum. It will deprecated soon.
  - `qiskit-ibmq-provider`: Access IBM Quantum. It has been deprecated by Qiskit.
