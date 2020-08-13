# boxel-adsb

A complete, functional ADS-B receiver system built from Boxel-provided Docker Compose configuration
and Docker containers.

## Usage / Install

Getting this running on a Raspberry Pi (or other embedded ARM-based computer) or even a PC/Mac is easy. Be sure you have Docker and Docker Compose
installed for your platform, and then follow these instructions.

1. Clone this repository to your system with `git clone git@github.com:boxelio/docker-compositions.git`.
2. Copy `.env.sample` to `.env` and edit all of the values to match your location and device.
3. Run `docker-compose up` to automatically pull down the docker images and get things running.
4. That's it!

## Components

| Name | Docker Image | Github | Description |
| ---- | ------------ | ------ | ----------- |
| airspy_adsb | [boxel/airspy-adsb](https://hub.docker.com/r/boxel/airspy-adsb) | [boxelio/dockerfiles](https://github.com/boxelio/dockerfiles/tree/master/flight/airspy-adsb) | Optimized ADS-B decoding using an Airspy SDR. This is fed into readsb. [OPTIONAL]|
| flightaware-skyview1090 | | | Map UI from FlightAware |
| mictronics-readsb | [boxel/mictronics-readsb](https://hub.docker.com/r/boxel/mictronics-readsb) | [boxelio/dockerfiles](https://github.com/boxelio/dockerfiles/tree/master/flight/mictronics-readsb) | ADS-B decoding using RTL-SDR, or just proxy from Airspy to the other apps. This feeds the web UIs as well as the exchanges. |
| mutability-mlat-client | | | MLAT client to feed ADSB Exchange (and others) |
| wiedehopf-graphs1090 | | | Graphs measuring data over time |
| wiedehopf-tar1090 | | | Map UI forked from dump1090 with many enhancements |

## More coming!

This docker composition is still young and a lot of changes will be coming to make this more flexible, more stable, and more comprehensive. Pull requests are welcome!
