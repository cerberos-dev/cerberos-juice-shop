# Cerberos OWASP Juice-shop
Dockerized version of the OWASP Juice shop (https://owasp.org/www-project-juice-shop/)

## Installation guide
1. `git clone https://github.com/cerberos-dev/cerberos-juice-shop.git`.
2. Copy `.env.example` to `.env`.
3. Edit `.env` to fit local environment.
4. Start containers: `docker-compose up -d`.

You can also start the containers and display debug information with: `docker-compose up`

## CTF
OWASP Juice Shop can be run in a special configuration that allows to use it in Capture-the-flag (CTF) events.

The configuration furthermore hides the GitHub ribbon in the top right corner of the screen. 
It also hides all hints from the score board. 

Instead it will make the solved-labels on the score board clickable which results in the corresponding "challenge solved!"-notification being repeated. 
This can be useful in case you forgot to copy a flag code before closing the corresponding notification.

If you want to enable CTF mode you need to set `NODE_ENV=ctf` in your .env file.

## Ports
Default the OWASP shop runs on port 3000, this can be changed to any port by setting `JUICE_SHOP_PORT=<desired port>`

## CTF Key
Default all instances have their own flags generated when ran in CTF mode. This provides issues when you run an actuall CTF. 
By setting the `CTF_KEY=<desired key>` you can make sure all flags are the same for all instances.

Default key: `Y2VyYmVyb3MtanVpY2Utc2hvcA==` (base64 encoded string: cerberos_juiceshop) in the example can be safely used.
