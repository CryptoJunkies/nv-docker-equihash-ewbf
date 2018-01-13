# nv-docker-equihash-ewbf [![Build Status](https://travis-ci.org/CultClassik/nv-docker-equihash-ewbf.svg?branch=master)](https://travis-ci.org/CultClassik/nv-docker-equihash-ewbf)
[Image on Docker Hub](https://hub.docker.com/r/cryptojunkies/ewbf/)

Dockerfile to build cryptojunkies/ewbf GPU container for mining Equihash based crypto currencies.

## Pre-requisites

Requires a working installation of Docker CE or EE and Nvidia-Docker2 and at least one NVidia GPU of course.

## Installation

docker build -t cryptojunkies/ewbf ./build

## Usage

docker run --runtime=nvidia -e "NVIDIA_VISIBLE_DEVICES=0" cryptojunkies/ewbf "--server mypool.net --port 1234 --user myusername --pass x --api 0.0.0.0:42000"

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

2018-13-01
Initial creation and build by CultClassik

## Credits

TODO: Write credits

## License

TODO: Write license