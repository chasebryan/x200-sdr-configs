# RTL-SDR Setup

This folder contains the minimal defaults I set up for the RTL-SDR Blog V4 on this machine.

Files:

- `sdr`: small launcher for common workflows
- `rtl-sdr-blacklist.conf`: kernel blacklist to keep the DVB driver from grabbing the dongle
- `gqrx-default.conf`: broadcast-FM startup preset for Gqrx
- `rtl-sdr-scan.desktop`: desktop launcher for the survey scan

Commands:

- `./sdr test`
- `./sdr fm`
- `./sdr fm 101.1e6`
- `./sdr gui`
- `./sdr scan 8`

Notes:

- `sdr test` is a short health check and exits cleanly.
- `sdr fm` defaults to `100e6`.
- `sdr scan` needs `gqrx` or another RTL-SDR process closed first because the dongle is single-claim.
- The current user is already in `plugdev`.
