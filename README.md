# RPI Domoticz

* Master : [![Circle CI](https://circleci.com/gh/zeiot/rpi-domoticz/tree/master.svg?style=svg)](https://circleci.com/gh/zeiot/rpi-domoticz/tree/master)
* Develop : [![Circle CI](https://circleci.com/gh/zeiot/rpi-domoticz/tree/develop.svg?style=svg)](https://circleci.com/gh/zeiot/rpi-domoticz/tree/develop)

Docker image of [Domoticz][] to use on a [Raspberry PI][].

Exposes Port `8080` 

Configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker):

    $ docker run --rm --privileged multiarch/qemu-user-static:register --reset

Then you can run an armhf image from your x86_64 Docker host :

    $ make run version=3.5

Or build :

    $ make build version=3.5


# Usage

Launch Domoticz :

    $ make run version=3.5


# Supported tags

* [![](https://images.microbadger.com/badges/version/zeiot/rpi-domoticz.svg)](http://microbadger.com/images/zeiot/rpi-domoticz "Get your own version badge on microbadger.com")


## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Raspberry PI]: https://www.raspberrypi.org/
[Mosquitto]: https://domoticz.com/
