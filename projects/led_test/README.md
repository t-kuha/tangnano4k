# Blinking LED

- Retrieved from https://github.com/sipeed/TangNano-4K-example/tree/main/led_test/project

```shell-session
$ yosys -p "read_verilog led_test.v; proc; synth_gowin; write_json synth.json"
$ nextpnr-gowin --json synth.json --write pnr.json --device GW1NSR-LV4CQN48PC6/I5 --cst led_test.cst
$ gowin_pack -d GW1NSR-LV4CQN48PC6/I5 -o led_test.fs pnr.json
$ openFPGALoader -m -b tangnano4k led_test.fs
```
