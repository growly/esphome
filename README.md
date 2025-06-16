# Wizard to pre-populate config files:

```
sudo docker run --rm -v "${PWD}":/config -it ghcr.io/esphome/esphome wizard <new-file>.yaml
```

# Compile and program

Note line (`/dev/ttyUSB0` in the example).

```
sudo docker run --rm --privileged -v "${PWD}":/config --device=/dev/ttyUSB0 -it ghcr.io/esphome/esphome run livingroom.yaml
```

# Using the templates with subsitutions

This basic feature of computing is called
"[substitutions](https://esphome.io/components/substitutions.html)" here.

```
esphome -s device_name gym config esp32-poe-template.yaml
```
