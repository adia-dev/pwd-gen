### Password Generator (pwd-gen)

The `pwd-gen` script is a versatile command-line tool designed to generate secure passwords using various cryptographic methods. It supports SHA-256, SHA-512, Base64 encoding, and MD5 hashing, providing flexibility for users to choose the level of security and password complexity that best fits their needs.

### Features

- **Multiple Hashing Algorithms**: Generate passwords using SHA-256, SHA-512, MD5, or Base64 encoding.
- **Interactive Mode**: Choose the password generation method via a user-friendly interactive menu.
- **Output Control**: Direct password output to a console or save directly to a file.
- **Verbose and Quiet Modes**: Get detailed execution logs or suppress all output, suitable for scripting and automation.

<img width="842" alt="Screenshot 2024-05-09 at 00 49 40" src="https://github.com/adia-dev/pwd-gen/assets/63371699/ca065d2b-e0de-456e-b995-70cacbfffc98">


### Installation

```bash
# Clone the repository
git clone https://github.com/adia-dev/pwd-gen.git

# Navigate to the script directory
cd pwd-gen

# Make the script executable
chmod +x pwd-gen.sh

# To install the script globally, move it to a directory in your PATH
ln -s "$(pwd)/pwd-gen.sh" /usr/local/bin/pwd-gen
```

### Usage

Basic command structure:

```bash
pwd-gen.sh [method] [options]
```

#### Methods

- `sha`: Generate a SHA-256 hashed password.
- `sha512`: Generate a SHA-512 hashed password.
- `base64`: Generate a Base64 encoded password.
- `md5`: Generate an MD5 hashed password (less secure).

#### Options

- `-it, --interactive`: Launch the script in interactive mode to select the password generation method.
- `--output-file [path]`: Save the generated password to a specified file.
- `--verbose`: Enable verbose output.
- `--quiet`: Suppress all output.

#### Examples

Generate a SHA-256 hashed password:

```bash
pwd-gen.sh sha
```

Generate a password in interactive mode and save to a file:

```bash
pwd-gen.sh --interactive --output-file /path/to/password.txt
```

Generate a Base64 encoded password and suppress all outputs:

```bash
pwd-gen.sh base64 --quiet
```

### Tested Environment

This script has been thoroughly tested on macOS, ensuring compatibility and reliability. For users on other Unix-like systems, minor adjustments may be necessary depending on available system utilities and Bash version.
