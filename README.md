# Fake mac address

Change network interface mac address on your Mac or Linux.

```
$ fake-mac-address

Pre-flight checks
› checking interface en5
  [  OK  ] interface en5 exists
› checking current mac address of interface en5
  [  OK  ] mac address isn't faked yet (00:00:5e:00:53:af)

Faking mac address
› invoke sudo
Password:
  [  OK  ] sudo authentication successfull
› fake mac address 00:15:e9:2b:99:3c
  [  OK  ] changing mac address
› restarting interface en5
  [  OK  ] stopping interface en5
  [  OK  ] starting interface en5
› verifying current mac address
  [  OK  ] mac address has been successfully faked
```

## Installation

**Important:** bash v3.2 and higher is required

1) Download archive from [the release page](https://github.com/Hologos/fake-mac-address/releases) and unpack it.
2) Create fma.cfg file (follow instructions in section [Configuration file](#configuration-file)).
3) Run the script.

### Dependencies

If on Linux, make sure you have all those things installed:

- `macchanger`: to change mac address

### Cloning repo

**Important:** _If you forget to do `peru sync` after every update that contained changed `peru.yaml`, it can have undesirable consequences and can cause serious problems. Use at your own risk._

_Downloading files from release page is preferred._

```bash
git clone https://github.com/Hologos/fake-mac-address
peru sync
```

## Description

### Usage

```
fake-mac-address [-c <config-filepath>]

    -c <filepath>
        Filepath to config file.

Environment variables
    FMA_CONFIG_FILEPATH - filepath to config file
```

You either have to specify the filepath to configuration file via an argument `-c` or you can set an environment variable `FMA_CONFIG_FILEPATH`.

### Configuration file

You need to provide a mac address you want to fake and network interface to affect.

```ini
fake_mac_address="00:15:e9:2b:99:3c"
affected_interface="en5"
```

## Keywords

- clone mac address
- cloning mac address
- change mac address
- changing mac address
