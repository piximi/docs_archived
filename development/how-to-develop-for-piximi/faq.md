---
description: 'Solutions to typical problems on development'
---

# Frequently asked questions

## Ubuntu related question

#### Cannot start new app due to watch error (Error: watch ... ENOSPC)

The solution is to increase the limit of inotify watchers (https://stackoverflow.com/questions/22475849/node-js-what-is-enospc-error-and-how-to-solve/32600959#32600959, technical details: https://github.com/guard/listen/wiki/Increasing-the-amount-of-inotify-watchers#the-technical-details):
```
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf
sudo sysctl -p
```
