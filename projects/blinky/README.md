# Blinking LED

- Based on https://github.com/YosysHQ/apicula/tree/master/examples

```shell-session
$ yosys -D LEDS_NR=8 -p "read_verilog blinky.v; proc; synth_gowin; write_json blinky.json"
$ nextpnr-gowin --json blinky.json --write pnrblinky.json --device GW1NSR-LV4CQN48PC6/I5 --cst tangnano4k.cst
$ gowin_pack -d GW1NSR-LV4CQN48PC6/I5 -o blinky.fs pnrblinky.json
$ openFPGALoader -m -b tangnano4k blinky.fs
```
