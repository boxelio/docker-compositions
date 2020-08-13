# boxel-adsb

A complete, functional ADS-B receiver system built from Boxel-provided Docker Compose configuration
and Docker containers.

## Components

| Name | Docker Image | Github | Description |
| ---- | ------------ | ------ |
| airspy_adsb | [boxel/airspy-adsb](https://hub.docker.com/r/boxel/airspy-adsb) | [boxelio/dockerfiles](https://github.com/boxelio/dockerfiles/tree/master/flight/airspy-adsb) | Optimized ADS-B decoding using an Airspy SDR. This is fed into readsb. [OPTIONAL]|
| mictronics-readsb | [boxel/mictronics-readsb](https://hub.docker.com/r/boxel/mictronics-readsb) | [boxelio/dockerfiles](https://github.com/boxelio/dockerfiles/tree/master/flight/mictronics-readsb) | ADS-B decoding using RTL-SDR, or just proxy from Airspy to the other apps. This feeds the web UIs as well as the exchanges. |
