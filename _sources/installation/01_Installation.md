# Installation

## By PyPI - Stable Release

- The package can be found in `pip list` as `qurrium-x.y.z`
- Pip downloads the most stable release, but not necessarily the latest version.

```bash
pip install qurrium
```

## By TestPyPI - Nightly Release

- This package can be found in `pip list` as `qurry-x.y.z.devW`
- This version includes new features and minor bug fixes, but may not be stable.

```bash
pip install qiskit tqdm requests
# the installation from testPyPI can' t find these dependencies
pip install -i https://test.pypi.org/simple/ qurry
```

## Maually by Git

**Qurry can be installed from source**. Since this package relies on Cython and Rust, **it requires "C complier" and "Rust complier" which you need to install first.**

To install rust, run the following command:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Then install `qurry` by the following command:

```bash
git clone https://github.com/harui2019/qurry-preview.git --recursive
cd qurry
pip install -e .
```

## Test Installation

`pytest` is used for testing. Simply run the following command after the installation:

```bash
pytest
```
