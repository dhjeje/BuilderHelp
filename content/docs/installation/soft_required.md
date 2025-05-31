---
weight: 4
title: "Required libraries and tools"
---

## Install required libraries and tools 

1. First, update and clean sources list
{{< highlight go-html-template >}}
apt-get update -yqq &&  apt-get install -y apt-utils
{{< / highlight >}}
then install this dependencies:
{{< highlight go-html-template >}}
apt-get update && apt-get install -y build-essential libpng-dev  locales zip jpegoptim optipng pngquant gifsicle unzip zip git curl lua-zlib-dev libmemcached-dev wget
{{< / highlight >}}


2. Install NodeJS 22.X
{{< highlight go-html-template >}}
curl -sL https://deb.nodesource.com/setup_22.x -o setup_22.sh
chmod +x setup_22.sh
sudo bash ./setup_22.sh
sudo apt-get install -y nodejs
{{< / highlight >}}

3. Install NPM
{{< highlight go-html-template >}}
wget https://www.npmjs.com/install.sh | sh
chmod +x install.sh
./install.sh
{{< / highlight >}}


4. Install Ionic 7
Before install Ionic, you must install NPM.
{{< highlight go-html-template >}}
npm i -g @ionic/cli@7
{{< / highlight >}}

5. Install PHP 8
Support ONLY PHP 8.1 and higher (in CGI and CLI mode). Before setup platform, you must configure your server for use PHP8 version in HTTP and console mode.
How to add PHP 8.1 to Ubuntu 20.xx:
{{< highlight go-html-template >}}
sudo apt update
sudo apt install lsb-release ca-certificates apt-transport-https software-properties-common -y
sudo add-apt-repository ppa:ondrej/php
sudo apt install php8.1
{{< / highlight >}}
check installed version:
{{< highlight go-html-template >}}
php -v
{{< / highlight >}}
Install this extensions:
{{< highlight go-html-template >}}
sudo apt install php8.1-mysql php8.1-zip php8.1-xml php8.1-dom php8.1-curl php8.1-common php-json php8.1-mbstring php-mysql php-curl php8.1-gd php8.1-xml
{{< / highlight >}}



# ⚠️ Attention!

**This library differs from the libraries used in the previous version**, so **simultaneous operation of both versions on the same server is not guaranteed**.

If you plan to install this version of the platform on a server with the older version, please note: **you do so at your own risk!**
