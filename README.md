# Hamming-74

This is only for 7 4 Hamming (7 output bits, 4 user bits, 3 parity bits)

The main concept used: XOR operation to calculate parity bits

Systematic Hamming is used (parity bits are placed at the end indexes)
ie the 3 parity bits are placed on index 4,5,6 on a 4 user bit signal


# Software
This project was executed using Emacs in a Ubuntu 20.04 Virtual Machine
(Dual boot using USB previously)

# Configuring Emacs
In Emacs, the files can be executed using F5.
During the first run, F5 might be undefined. This is because the .emacs directory is in the root instead of $home.

The steps to configure this:
1. sudo cp ~root/.emacs ~/  
2. ls -la .emacs
3. sudo chown (user):(group) .emacs
(eg sudo chown ubuntu:ubuntu .emacs)

# If make command is not found
1. sudo apt-get install -y make
2. sudo apt install build-essential

