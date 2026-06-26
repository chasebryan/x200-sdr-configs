# RTL-SDR Setup

This folder contains the minimal defaults I set up for the RTL-SDR Blog V4 on this machine.

Files:

- `sdr`: small launcher for common workflows
- `rtl-sdr-blacklist.conf`: kernel blacklist to keep the DVB driver from grabbing the dongle
- `gqrx-default.conf`: broadcast-FM startup preset for Gqrx
- `rtl-sdr-scan.desktop`: desktop launcher for the survey scan
- `rtl-sdr-scan.png`: icon for the survey scan launcher
- `bookmarks.csv`: generated Gqrx bookmarks from the latest scan

Commands:

- `./sdr test`
- `./sdr fm`
- `./sdr fm 101.1e6`
- `./sdr weather`
- `./sdr sarnet`
- `./sdr scan 8`
- `./sdr import-scan`
- `./sdr gui`

Notes:

- `sdr test` is a short health check and exits cleanly.
- `sdr fm` defaults to `100e6`.
- `sdr weather` starts Gqrx in narrow FM on NOAA Weather Radio with a ready-to-use preset.
- `sdr sarnet` starts a narrow-FM emergency-net search preset centered on 2m simplex so you can work Florida-style SARNET traffic without guessing a random mode.
- `sdr scan` needs `gqrx` or another RTL-SDR process closed first because the dongle is single-claim.
- `sdr import-scan` writes `bookmarks.csv` into your active Gqrx config dir (`$XDG_CONFIG_HOME/gqrx` or `~/.config/gqrx`), which Gqrx loads on startup.
- The current user is already in `plugdev`.
