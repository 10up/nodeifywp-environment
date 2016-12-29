# NodeifyWP Environment

[NodeifyWP](https://github.com/10up/nodeifywp) is a framework that let's you create isomorphic JavaScript applications with WordPress and PHP. The framework relies on the PHP extension [V8JS](https://github.com/phpv8/v8js) and [Google V8](https://developers.google.com/v8/) which can be time consuming to install and optimize. This repository contains a Dockerized environment for running NodeifyWP WordPress applications.

<p align="center">
<a href="http://10up.com/contact/"><img src="https://10updotcom-wpengine.s3.amazonaws.com/uploads/2016/10/10up-Github-Banner.png" width="850"></a>
</p>

## Requirements

* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/)
* [Composer](https://getcomposer.org/)

## Setup

The project contains a fully-fledged Docker based environment. Ensure your machine meets the project requirements before following these steps.

1. From the root of the repository, run the following in the command line:
  
  `composer install`

  This installs WordPress, [Twenty Sixteen React](https://github.com/10up/twentysixteenreact), a NodeifyWP theme, and a few debug plugins.
2. From the root of the repository, run the following in the command line:
  
  `docker-compose up`

  This starts up the environment. This may take awhile the first time as you need to download the Docker images.
3. In your browser navigate to `http://localhost`
4. Run through WordPress install steps. Here is the database information you'll need to use:
  
  * MySQL Host: *mysql*
  * Database Name: *wordpress*
  * Database Username: *root*
  * Database Password: *password*
5. Activate the Twenty Sixteen React theme.

## Environment

The project environment contains the following:

* PHP-FPM 7
* Nginx
* Redis
* MariaDB

By default the project includes Redis for caching but does not instruct WordPress to do anything with it. If you want caching, you'll need the drop-ins, [WP Redis](https://github.com/pantheon-systems/wp-redis) and [Batcache](https://github.com/Automattic/batcache).

## License

This is free software; you can redistribute it and/or modify it under the terms of the [GNU General Public License](http://www.gnu.org/licenses/gpl-2.0.html) as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.
