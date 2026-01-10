# QMK keymaps for my keyboard


### Instalation

Clone the wireless_playground branch of the keychron qmk fork. (I like having it in my Builds folder).
```bash
git clone -b wireless_playground https://github.com/Keychron/qmk_firmware.git
cd qmk_firmware
```

Install qmk
```bash
sudo apt install qmk
```
Setup qmk with the home folder being the **qmk_firmware fork from keychron**!! Answer yes to prompts as reasonable.
```bash
qmk setup -H .
qmk doctor
```

Copy the keymap from this project into they keyboard keymaps folder

```bash
qmk compile -kb keychron/v6_max/ansi_encoder -km adaubner
```

### Flashing

Switch the keyboard to cable mode. Hold the esc key while plugging it in to put it into flash mode. With a second keyboard:
```bash
qmk flash -kb keychron/v6_max/ansi_encoder -km adaubner
```

To turn off the ugly lights press fn + light key