# Memory-Encrypted-Virtual-Machine
Normal virtual machines are vulnerable to a "Cold boot attack", where by an adversary posing as a UniCoin miner can attack their customers, stealing secret keys! To get around this: We use a ChromeOS inspired bootloader, encrypt all the memory used by the VM, and clear all the keys from the CPU registers upon any reboot/powerstate change
