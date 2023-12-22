# Memory-Encrypted-Virtual-Machine
Normal virtual machines are vulnerable to a "Cold boot attack", where by an adversary posing as a UniCoin miner can attack their customers, stealing secret keys! To get around this: We use a ChromeOS inspired bootloader, encrypt all the memory used by the VM, and **clear all the keys from the CPU registers** upon any reboot/powerstate change or detection of unknown hardware, or power state change.

The only way to attack this system, is to have a cleanroom lab reverse engineer & modify the CPU before building the mining node! We can defend against this by having a "Key Vault" functional unit sadwitched inside the CPU at the middle layer, making it virtally impossible to get to without destroying the chip. This will contain a private key, which when paired with a secure "Oracle Node" in the network can verify that the Miner is running a know secure & unaltered CPU!

# Defending against:
## Bus Pirates
Even a "Bus Pirate" reading the memory bus cannot decrypt it! Only data sent to peripherals like the Network card can be partially read. Excluding any data/fields which were encrypted on the CPU and sent in that form.

# Technology & Architecture:
## Memory Encryption
sch: https://www.google.com/search?q=IBM+encrypted+virtual+machine, https://www.google.com/search?q=memory+encryption, https://www.google.com/search?q=memory+encryption+virtual+machine
- https://research.ibm.com/publications/encrypted-virtual-machine-images-for-confidential-computing
- https://www.amd.com/content/dam/amd/en/documents/epyc-business-docs/white-papers/memory-encryption-white-paper.pdf

## AMD Secure Encrypted Virtualization (SEV)
https://www.amd.com/en/developer/sev.html
