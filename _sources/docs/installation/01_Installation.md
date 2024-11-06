# Installation

## By PyPI - Stable Release

- Would show up in `pip list` as `qurrium-x.y.z`

```bash
pip install qurrium
```

## By TestPyPI - Nightly Release

- Would show up in `pip list` as `qurry-x.y.z.devW`

```bash
pip install qiskit qiskit-aer tqdm requests
# the installation from testPyPI can' t find these dependencies
pip install -i https://test.pypi.org/simple/ qurry
```

## Maually by Git

**This method is installed from source**, since we introduce Rust, **it will require "Rust complier" you need to install first.**

You can install rust quickly by the following command:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Then, you can install `qurry` by the following command:

```bash
git clone https://github.com/harui2019/qurrium.git --recursive
cd qurry
pip install -e .
```

We have pytest for testing, you can run the following command to test:

```bash
pytest
```

After you finish the installation and want to comfirm the installation.
