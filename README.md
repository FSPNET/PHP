# Docker-PHP

FSP Network Gen2 Server Infrastructure - PHP

[![MicroBadger Size](https://img.shields.io/microbadger/image-size/fspnetwork/php.svg?style=flat-square)](https://microbadger.com/#/images/fspnetwork/php)
[![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/php.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/php/)
[![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/php.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/php/)
[![GitHub](https://img.shields.io/github/license/fspnet/php.svg?style=flat-square)](https://github.com/fspnetwork/php/blob/master/LICENSE)
![PHP Version](https://img.shields.io/badge/PHP-7.2-blue.svg?style=flat-square)

## Usage

```bash
docker run -d --restart=unless-stopped --name php --network net-fsp -v /opt/www:/data/www:rw -v /opt/php/log:/var/log/php-fpm fspnetwork/php
```

**Or**

```bash
docker-compose up -d
```