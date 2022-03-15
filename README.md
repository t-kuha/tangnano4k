# tangnano4k

Sipeed TangNano 4K projects

## Tool version

- Gowin IDE: V1.9.8.02
- [yosys](https://github.com/YosysHQ/yosys): yosys-0.13
- [apicula](https://github.com/YosysHQ/apicula): git rev. 9461235
- [nextpnr](https://github.com/YosysHQ/nextpnr): git rev. fbeef2b8

## How to set up environment

```shell-session
:: Linux & Mac
$ export PATH=$(pwd)/python/bin:$(pwd)/tools/$(uname)/bin:${PATH}
:: Only Mac
$ export DYLD_LIBRARY_PATH=$(pwd)/python/lib
```

## Programming TangNano 4k board

```shell-session
# program SRAM
$ openFPGALoader -m -b tangnano4k <bitstream>

# program FLASH
$ openFPGALoader -f -b tangnano4k <bitstream>
```

***

## References

- Sipeed Wiki: https://wiki.sipeed.com/hardware/zh/tang/Tang-Nano/Nano-4K.html
- Sipeed GitHub: https://github.com/sipeed/TangNano-4K-example
- Tool Download: http://www.gowinsemi.com.cn/faq.aspx
- openFPGALoader: https://github.com/trabucayre/openFPGALoader
- openFPGALoader doc: https://trabucayre.github.io/openFPGALoader/
- DVI TX ref design by timschuerewegen: https://github.com/timschuerewegen/tang-nano-4k
- New clean hdmi implementation by splinedrive: https://github.com/splinedrive/my_hdmi_device
