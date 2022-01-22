# tangnano4k

Sipeed TangNano 4K projects

## How to set up environment

```shell-session
$ export PATH=$(pwd)/python/bin:$(pwd)/tools/$(uname)/bin:${PATH}
```

## Programming device

```shell-session
# program SRAM
$ tools/$(uname)/bin/openFPGALoader -m -b tangnano4k <bitstream>

# program FLASH
$ tools/$(uname)/bin/openFPGALoader -f -b tangnano4k <bitstream>
```

***

## References

- Sipeed Wiki: https://wiki.sipeed.com/hardware/zh/tang/Tang-Nano-4K/Nano-4K.html
- Sipeed GitHub: https://github.com/sipeed/TangNano-4K-example
- Tool Download: http://www.gowinsemi.com.cn/faq.aspx
- openFPGALoader: https://github.com/trabucayre/openFPGALoader
- openFPGALoader doc: https://trabucayre.github.io/openFPGALoader/
