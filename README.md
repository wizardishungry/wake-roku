# wake-roku
Wake my roku and set the input to correct hdmi when shairport-sync playback is triggered. HDMI2 is hardcoded.

The Roku is discovered using `gssdp-discover` and the endpoint is cached in `~/.roku`.

## shairport-sync how-to
On Raspberry Pi:

1. Install tools `sudo apt install -y shairport-sync ruby gupnp-tools`
2. Edit `/etc/shairport-sync.conf`.
```
run_this_before_play_begins = "/home/pi/wake-roku/wake-roku"; // or whatever path
```
3. Restart service `sudo systemctl restart shairport-sync.service`

# Docs

* [Roku External Control API](https://sdkdocs.roku.com/display/sdkdoc/External+Control+API)
* [shairport-sync](https://github.com/mikebrady/shairport-sync)
