# Docker-PHP

FSP Network Gen2 Server Infrastructure - PHP

[![MicroBadger Size](https://img.shields.io/microbadger/image-size/fspnetwork/php.svg?style=flat-square)](https://microbadger.com/#/images/fspnetwork/php)
[![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/php.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/php/)
[![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/php.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/php/)
[![GitHub](https://img.shields.io/github/license/fspnet/php.svg?style=flat-square)](https://github.com/fspnetwork/php/blob/master/LICENSE)

## Usage

- [`7.2` (72/Dockerfile)](https://github.com/FSPNet/PHP/blob/master/72/Dockerfile)
- [`7.3`, `latest`, `stable` (73/Dockerfile)](https://github.com/FSPNet/PHP/blob/master/73/Dockerfile)

```bash
docker run -d --restart=unless-stopped --name php --network net-fsp -v /opt/www:/data/www:rw -v /opt/php/log:/var/log/php-fpm fspnetwork/php
```