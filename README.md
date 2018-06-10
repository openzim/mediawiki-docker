OpenZIM Mediawiki Docker
========================

OpenZIM Mediawiki Docker offers a straight forward solution to deploy
Mediawki within on ly one Docker container.

Run
---

To create your Docker container:

```
sudo docker pull -a openzim/mediawiki
mkdir -p data 
sudo docker run -p 8080:80 \
  -v <YOUR_CUSTOM_DATA_DIRECTORY>:/var/www/data -it openzim/mediawiki
```

Connect to your Docker container with your browser at
http://localhost:8080/

User credentials
----------------

user: Admin
pass: adminadmin

Customise
---------

The `data` directory contains the database, images, file config and
images.

You can customise the Mediawiki by editing your
`LocalSettings.custom.php`. If you want to know more, have a look to
this documentation:
https://www.mediawiki.org/wiki/Manual:LocalSettings.php

Backup
------

All your data are available in your `<YOUR_CUSTOM_DATA_DIRECTORY>`
data directory.

Build yourself own Docker image
-------------------------------

```
docker build -t my_mediawiki docker 
```
