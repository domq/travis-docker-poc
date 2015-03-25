# travis-docker-poc
Proof of concept for running your Travis test suite in Docker

## Lab Book

### Build 1: Why doesn't it work to just run docker -d from a Travis VM?

Because the kernel of that VM lacks certain network features.

[pid 5845] socket(PF_INET, SOCK_DGRAM, IPPROTO_IP) = 4
[pid 5845] ioctl(4, SIOCBRADDBR, 0xc2083ec018) = -1 ENOPKG (Package not installed)

[pid 5845] write(2, "\33[34mINFO\33[0m[0000] -job init_networkdriver() = ERR (1) \n", 66INFO[0000] -job init_networkdriver() = ERR (1)

) = 66

[pid 5845] write(2, "\33[31mFATA\33[0m[0000] package not installed \n", 66FATA[0000] package not installed

) = 66

