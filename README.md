![image_2021-06-25_19-20-52](https://user-images.githubusercontent.com/86243750/123417606-8d9ef300-d5ea-11eb-916d-f396e82ec700.png)
# First and Foremost

From my own experience, you need to priorities the model of your own motherboard because theres a lot of tweaks (ACPI) for a particular board. So I only recommended people with same board as me to try the EFI.

I didnt enable above 4G decoding on my bios, instead i put npci=0x2000 at boot-args. If you want to enable it, delete this command manually. npci=0x2000 disables some PCI debugging related to kIOPCIConfiguratorPFM64, alternative is npci= 0x3000 which disables debugging related to gIOPCITunnelledKey in addition. Required for when getting stuck on PCI Start Configuration as there are IRQ conflicts relating to your PCI lanes. Not needed if Above4GDecoding is enabled.

# Specification

First build on Hackintosh on PC with a specification:
1) Processor	AMD Ryzen 3 PRO 4350G with Radeon Graphics, 3801 Mhz, 4 Core(s), 8 Logical Processor(s)
2) BaseBoard Manufacturer	ASRock A520M-HDV
3) Installed Physical Memory (RAM)	16.0 GB
4) RX 580 4GB
5) 250GB NVMe (Windows), 500GB SATA HDD (Hackintosh), 1TB SATA HDD (Data for both OS)

# Bugs and Troubleshooting

This build is beta, so few of bugs is expected.
(edit 1= it seems have problem with abovr 4G Decoding on bios setup. Removing an argument at boot-args will solve the problem)




