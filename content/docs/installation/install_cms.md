---
weight: 7
title: "Install Moxly App Builder"
---

# Install Moxly App Builder

## Steps
After install all requred dependencies and tools, you can install platform.

Аollow these steps:
- Set the domain name to be used for the platform
- Setup domain dir in server
- Install an SSL certificate, since the platform only works with a secure connection.
- Create MySQL database
- Upload install.zip to domain folder and unpack.

After then, open your domain url in browser and make install with follow the instructions.

## Add a Scheduler

**You must add this command to cron:**
{{< highlight go-html-template >}}
php /path/to/your/domain/artisan schedule:run  >/dev/null 2>&1 
{{< / highlight >}}
This cron job mut be running every minuts