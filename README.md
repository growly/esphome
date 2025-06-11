# Wizard to pre-populate config files:

```
sudo docker run --rm -v "${PWD}":/config -it ghcr.io/esphome/esphome wizard <new-file>.yaml
```

# Compile and program

Note line (`/dev/ttyUSB0` in the example).

```
sudo docker run --rm --privileged -v "${PWD}":/config --device=/dev/ttyUSB0 -it ghcr.io/esphome/esphome run livingroom.yaml
```
