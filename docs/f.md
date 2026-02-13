# Small File
I save a small file in the root of the directory and then re-examine.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig10.png">
<figcaption>Fig 10. The directory.</figcaption>
</figure>

I extract the bytes relating to the new file entry, note there is also a Recycle Bin entry. File names were originally 8:3, but with Long File Names (LFNs) bytes:

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig11.png">
<figcaption>Fig 11. The directory, decoded.</figcaption>
</figure>

The first 32 bytes are the LFN entry.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig12.png">
<figcaption>Fig 12. LFN.</figcaption>
</figure>

The next 32 bytes are the same format as the original directory before LFN.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig13.png">
<figcaption>Fig 13. Directory entry.</figcaption>
</figure>

FAT1 is located at cluster 128 + 4 = 132 or byte 65,536 + 2,048 = 67,584. THE FAT is very simple, almost empty. Each entry is 16 bits, so cluster 0x05 is as shown, with a value of 0xFFFF. This makes sense, it’s a file with less than 512 bytes, it occupies a single cluster.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig14.png">
<figcaption>Fig 14. Decoding.</figcaption>
</figure>

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig15.png">
<figcaption>Fig 15. WinHex the sector.</figcaption>
</figure>

