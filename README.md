## What is this?

In Linux, it can be a pain when you want to create a hotspot with full feature & bandwidth. For example, `nm-connection-editor` can help you create a hotspot but it will be handicapped to 2.4GHz even if your card is capable of 5GHz. This script allows you to create a much more customizable hotspot (5GHz, channel selection, mode selection, wifi 7, etc.)

## Getting started

Make sure you have `iw`, `hostapd` and `dnsmasq` installed

Put `create_ap` somewhere your `PATH` can see (or you can add the directory of this repo to your `PATH`)

Default config and hotspot toggle script are in the `examples` folder

Easiest way to use is to call the `toggle-hotspot` when you want your hotspot on/off (with the correct path to the config file and the `WIFI_IFACE` and `INTERNET_IFACE` set correctly). The default config file works for my setup with a not-too-advanced wifi card so hopefully it'll work for you too (I use Arch Linux)

## FAQs

`How do I know WIFI_IFACE and INTERNET_IFACE?`

`INTERNET_IFACE` is the interface of your ethernet connection or the card connecting to your router, `WIFI_IFACE` is the interface of the card you want to host the hotspot on. For my case, both are set to `wlp9s0` but yours may differ. You can find out yours by running `ip addr`