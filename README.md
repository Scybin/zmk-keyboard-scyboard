# ZMK Module: scyboard Keyboard

This repository provides shield files for the [scyboard](https://github.com/Scybin/scyboard) keyboard. It can be used to build the ZMK firmware for the keyboard.

## Usage

Edit your west.yaml file found in your zmk config's config directory to add the scyboard module.

Example:

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: scybin
      url-base: https://github.com/scybin
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboard-scyboard
      remote: scybin
      revision: main
  self:
    path: config
```

My personal ZMK firmware configuration can be found [here](https://github.com/Scybin/zmk-config-scyboard).

## More Info

For more info on modules, you can read through the [Zephyr modules page](https://docs.zephyrproject.org/3.5.0/develop/modules.html) and [ZMK's page on using modules](https://zmk.dev/docs/features/modules). [Zephyr's west manifest page](https://docs.zephyrproject.org/3.5.0/develop/west/manifest.html#west-manifests) may also be of use.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.txt) file for details.
