# NVMe Support on Intel DQ77KB

 Intel dq77kb NVMe support

 - Since Intel performs signature verification on bios flashing
 - A method to modify the firmware by read and flash it with CH341A programmer

## NvmExpressDxe_4.ffs

 - Size: 20,832 B
 - MD5 HASH: A74EFB965565A6F48498ED1C7B7C2A8B
 - SHA-1 HASH: 3C4C8E83DC5924EDBECB3299F7BDB2BCAF1AD867
 - Verify hash in powershell

```sh
    CertUtil -hashfile ./NvmExpressDxe_4.ffs MD5
    CertUtil -hashfile ./NvmExpressDxe_4.ffs SHA1
```

## [UEFITool](UEFITool.exe) Version

 - 0.26.0

## Read BIOS Image from Chip

 - CH341A
 - bios-8M-25Q64FV
 - [bios-8M-25Q64FV.bin](bios-8M-25Q64FV.bin)

![bios-8M-25Q64FV.png](readme%2Fbios-8M-25Q64FV.png)

 - bios-4M-25Q32BV
 - [bios-4M-25Q32BV.bin](bios-4M-25Q32BV.bin)

![bios-4M-25Q32BV.png](readme%2Fbios-4M-25Q32BV.png)

## Merge Bios Image

------------------------

    BIOS IMAGE = <8M FILE> + <4M FILE>

------------------------

 - [bios-backup-8M+4M-merged.bin](bios-backup-8M%2B4M-merged.bin)

## Modify Bios Image

 - Reference [Get NVMe support on unsupported bios with BIOS modding.pdf](readme%2FGet%20NVMe%20support%20on%20unsupported%20bios%20with%20BIOS%20modding.pdf)
 - [bios-Nvme-patch-8M+4M-merged.bin](bios-Nvme-patch-8M%2B4M-merged.bin)

## Split Bios Image

 - The end position of the new bios file is 8M (8388608 B)
 - Through comparison, it was found that the changes were in the 4M BIOS file.
 - [bios-4M-25Q32BV-Nvme-patch.bin](bios-4M-25Q32BV-Nvme-patch.bin)

## Use CH341A to flash New 4M BIOS File to the bios-4M-25Q32BV Chip

## ENJOY!