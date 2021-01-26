# Homestead box of streamfiuse 

## Mac - Homestead.yaml
```yaml
---
ip: "192.168.10.10"
memory: 2048
cpus: 2
provider: virtualbox

authorize: ~/.ssh/id_rsa.pub

keys:
    - ~/.ssh/id_rsa

folders:
    - map: ~/Documents/laravel/code
      to: /home/vagrant/code

sites:                                      #add the urls dev.streamdfiuse.____ under the ip 192.168.10.10 in /etc/hosts
    - map: dev.streamfiuse.core 
      to: /home/vagrant/code/core/public
    - map: dev.streamfiuse.web
      to: /home/vagrant/code/web/public

databases:
    - streamTinder

features:
    - mysql: true
    - mariadb: false
    - postgresql: false
    - ohmyzsh: true
    - webdriver: false

#services:
#    - enabled:
#        - "postgresql@12-main"
#    - disabled:
#        - "postgresql@11-main"

# ports:
#     - send: 50000
#       to: 5000
#     - send: 7777
#       to: 777
#       protocol: udp

```
