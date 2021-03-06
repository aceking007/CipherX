# CipherX
*cipherx* is a CLI tool and python library that provides solutions to encrypting and decrypting files using various ciphers.

The library is compatible with Python 3.6 and above, and does not depend on external packages (uses only the Python standard library).  
|||
|-|-|
|Author   | Arpit "aceking" Omprakash             |
|License  | MIT License                           |
|Homepage | https://github.com/aceking007/CipherX |

## Supported Ciphers

The following ciphers are currently supported:
1. Caesar Cipher
2. ROT 13 Cipher

## Installing
<!--
The easiest way to install the library is to execute (possibly in a virtualenv) the command:  

```
pip install cipherx
```

(note that you need network access to do it this way; if you do not have the *pip* tool installed - see: https://pip.pypa.io/en/latest/installing.html)
-->

Currently, the software is in its testing phase and has minimal features. The current version on GitHub is v0.1.0  

You can [download](https://github.com/aceking007/CipherX) the source code as zip, unpack it, `cd` to the unpacked directory and execute the following command:

```
python setup.py install
```

Alternatively, you can download the tar-ball from the [GitHub release](https://github.com/aceking007/CipherX/releases/), `cd` to the directory of the tar-ball, and use the pip install command to install the software:

```
pip install cipherx-0.1.0.tar.gz
```

(you may need to have administrator privileges and/or network access, especially if you are executing it *not* in a *virtualenv*).

## Usage

```
python -m cipherx [in_file] [out_file] [-flags] [-optional_arguments {parameters}]
```

**Positional Arguments**  

The script takes two positional arguments:
- `in_file` : The path to the input file (file containing text to be encrypted or decrypted)
- `out_file` : The path to the output file (file is created if not present)

**Optional Arguments and Flags**  

| Short | Long    | Parameters  | Default | Description |
|-------|---------|-------------|---------|-------------|
| -c    | -cipher | Integer between 1 and 3 | 1 | Indicates the cipher to be used |
| -s    | -shift  | Integer between 1 and 36 | 3 | The shift for Caesar Cipher |
| -d    | -decrypt| - | - | Turn this flag on to enable decryption |

**Cipher Table**

The following table indicates the parameter for the `cipher` argument above and the corresponding cipher that is invoked:

| Parameter | Cipher Used |
|-----------|-------------|
| 1 | Caesar Cipher|
| 2 | ROT 13 |

**An example**  
The following code uses the `Caesar Cipher` with a shift value of `10` to `decrypt` text from the file `in.txt` and store it in the output file named `out.txt` :

```
python -m cipherx in.txt out.txt -d -c 1 -s 10
```

## Using submodules

The package ships with different submodules that one can use for their own projects or codes. The submodules have code for the different ciphers implemented. Here is the partial package structure showing all the sub-packages and submodules that you can use in your own codes:

```
cipherx/
  ciphers/
    caesar_cipher.py
```
