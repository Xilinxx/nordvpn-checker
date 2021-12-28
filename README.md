# nordvpn-checker

A simple Python script to check if NordVPN accounts listed in a file are valid.

## NOTE: This script only works in Linux.

# Requirements

- The NordVPN CLI tool. [Get it from here](https://nordvpn.com/download/linux/).
- [Python 3.7](https://www.python.org/downloads/).
- An input file containing NordVPN login entries in `email:password` format.

# Installation

- Clone the repo with `git clone https://github.com/behnambm/nordvpn-checker`

# Code format
The Uncompromising Code Formatter [Black](https://github.com/psf/black5)

```
black -t py38 nord-checker.py
```

# Usage

- The syntax is
  > `nord-checker.py [--file | -f] path/to/file [--output | -o] path/to/file [--connect | -c] [--delete | -d]`

For example, `cd` into the recently cloned directory and run:

```
$ python nord-checker.py --file accounts.txt --output success.txt
```

If you just want to connect you can use: 
(The first successful connection will exit this script)

```
$ python nord-checker.py --file succes.txt --output /dev/null -c
```


- Unique successful entries are appended to the specified output file.
- The faulty entries will be removed from the input_file (requires sed)

# Best Practice
Have your router connected to NordVPN. After 50 attempts you will get blocked.
Then change your NVPN server and you are good to go again.

# Ideas
* When making a connection, use the best available server (lowest load)
* order the output-list alphabetical
* have the expire date in the output list 'email:password | date' 
* don't add inactive accounts to the output

### Contact

- [My Telgram](https://t.me/behnam_1121)
- volunteer [Xilinxx](https://t.me/xilinxx)
