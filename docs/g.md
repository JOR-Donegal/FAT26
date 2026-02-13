# Larger File
Next, I saved a JPEG file to the partition, (Narrow MugShot-JOR.JPG). A quick look at the directory entry gives me a starting cluster of 0x08.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig16.png">
<figcaption>Fig 16. Directory Entry.</figcaption>
</figure>

I can see a file that spans more than one cluster! In cluster 0x08 there is a pointer to the next cluster with parts of the file, 0x09. This continues in sequence for 12 cluster until cluster 19 has the EOF value, 0xFFFF.

<figure>
<img src = "https://jor-donegal.github.io/FAT26/images/fig17.png">
<figcaption>Fig 17. FAT.</figcaption>
</figure>

