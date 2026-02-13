# Interpreting the Structure

Using techniques from the previous practical on partition tables, I read the MBR partition table and located the first partition.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig1.png">
<figcaption>Fig 1. WinHex.</figcaption>
</figure>

I extracted the first partition table entry.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig2.png">
<figcaption>Fig 2. Partition Table.</figcaption>
</figure>

- The partition is not bootable
- Partition type is 0x0C, FAT32 or 0x0E for FAT16
- LBA starts at 0x00000080 (4 bytes, little endian) and with 512-byte - Sectors, this gives a start of 0x80 * 51210 = 65,536
- LBA ends at 0x001F2800 (4 bytes, little endian) or sector 2,041,856

Now I can locate the start of the FAT partition at sector 128, address 65,536.