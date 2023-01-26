# Stick Deck

Turn your Steam Deck as a bluetooth joystick(gamepad) on PC.

> **Note**: This solution doesn't implement HID (Human Interface Device), so you have to run a receiver program on your PC.

<iframe src="//player.bilibili.com/player.html?aid=948272039&bvid=BV19s4y1x7KM&cid=980233910&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

## Prerequisites

For both PC and Steam Deck:

- Python 3.x
- PyBlueZ

> **Warning**: Install PyBlueZ by using its source code, **_DON'T_** just `pip install pybluez`, you should `git clone git@github.com:pybluez/pybluez.git` then `python setup.py install`.

> **Note**: For PC when installing PyBlueZ, you might need to install Windows C++ SDK. Just follow the tips from the pybluez.

Additional requirements for PC:

- `pip install vgamepad`, this will install a virtual gamepad driver on your PC.

Additional requirements for Steam Deck:

- `pip install pyjoystick`

> **Note**: During the installations above, you might need to install some additional softwares. Just follow those error messages and install them manually.

## Run the Sender on Steam Deck

First, set your bluetooth visible: Settings - Bluetooth - Configure - Visible

> **Note**: Or you can use `bluetoothctl` and `discoverable on`.

```bash
python deck.py
```

## Run the Receiver on PC

```bash
python win.py <address> [port=1]
```

> **Note**: You can debug the joystick by running `joy.cpl` utility on Windows.
