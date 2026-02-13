# The Root Directory
To locate the root directory;
- Each sector is 512 bytes
- The file system starts at sector 128
- The reserved area is 4 sectors
- There are 2 FATs
- Each FAT is 250 sectors
- The root directory should be 632 sectors in or at byte 323,584.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig7.png">
<figcaption>Fig 7. Interpret the EBPB.</figcaption>
</figure>

I now navigate to the correct sector and verify that there appears to be an empty root directory, on a volume called RUBBISH (first 32 bytes). Byte 0x0B has a value 0x08, the table shows this to be a volume label.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig8.png">
<figcaption>Fig 8. Byte table.</figcaption>
</figure>

In the next two groups of 32 bytes, byte 0x0B is set to 0x0F. This marks the entry as system/hidden/read only. The final group of 32 bytes has an attribute 0x16, this marks the entry as subdirectory/system/hidden.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig9.png">
<figcaption>Fig 9. The directory.</figcaption>
</figure>


