# Simple Shell

![C Language](https://img.shields.io/badge/Language-C-blue)

<h3 align="center">
<img src="https://cdn.rawgit.com/odb/official-bash-logo/master/assets/Logos/Identity/PNG/BASH_logo-transparent-bg-color.png">
</h3>

## Table of Contents
- [Description](#description)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [Interactive Mode](#interactive-mode)
  - [Non-Interactive Mode](#non-interactive-mode)
- [File Structure](#file-structure)
- [Flowchart](#flowchart)
- [Contributing](#contributing)
- [Authors](#authors)

## Description
Simple Shell is a command-line interpreter that provides a user interface to access operating system services. This implementation is written in C and mimics the behavior of the sh shell with specific features and limitations.

## Features
- Displays a prompt and waits for the user to type a command
- Handles command lines with arguments
- Handles the PATH to find programs
- Implements built-in commands:
  - `exit` - exits the shell
  - `env` - prints the current environment
  - `cd` - changes directory
  - `help` - displays help information
- Handles command separators (`;`)
- Supports logical operators (`&&` and `||`)
- Handles comments (`#`)
- Supports variables replacement
- Handles the `$?` variable
- Handles the `$$` variable

## Requirements
- Ubuntu 20.04 LTS
- gcc compiler (with flags: -Wall -Werror -Wextra -pedantic -std=gnu89)

## Installation
```bash
git clone https://github.com/Adameelmadani/simple_shell.git
cd simple_shell
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

## Usage
### Interactive Mode
```bash
$ ./hsh
($) /bin/ls
hsh main.c shell.c shell.h
($) exit
$
```

### Non-Interactive Mode
```bash
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c shell.h
$
```

## File Structure
- **main.c**: Entry point of the program
- **shell.h**: Header file with function prototypes and structures
- **shell.c**: Main shell implementation
- **builtins.c**: Implementation of built-in commands
- **parser.c**: Command parsing functions
- **executor.c**: Command execution functions
- **helpers.c**: Helper functions
- **memory.c**: Memory management functions

## Flowchart
```
+-------------+     +-----------+     +------------+     +-----------+
| Read Input  |---->| Parse     |---->| Execute    |---->| Display   |
|             |     | Command   |     | Command    |     | Result    |
+-------------+     +-----------+     +------------+     +-----------+
        ^                                                      |
        |                                                      |
        +------------------------------------------------------+
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Authors
- [@Adameelmadani](https://github.com/Adameelmadani)
- [@henrychris](https://github.com/henrychris)
