# ABDocker-arm
Unofficial arm7 Dockerfile for AwesomeBot by BitQuote: https://github.com/BitQuote/AwesomeBot 

AwesomeBot: https://github.com/BitQuote/AwesomeBot/wiki

You will need to apply for a self-hosting token from BitQuote: http://self-host.awesomebot.xyz/

Prerequisites:
* Docker https://docs.docker.com/engine/installation/
* Git
* arm7 processor (rpi, arduino, etc)

<strong>For the x64 version of this please head to https://github.com/taylorsmcclure/ABDocker</strong>

1) Download auth.json and fill in the values https://github.com/BitQuote/AwesomeBot/wiki/Setup
2) Download config.json for modifiable configurations outside of the container
3) Run the bot attached on first run 
```
docker run -it --rm -v /path/to/auth.json:/node_modules/AwesomeBot/auth.json \
-v /path/to/config.json:/node_modules/AwesomeBot/data/config.json \
-p 0.0.0.0:80:8080 \
--name your_container \
-t taylorsmcclure/abdocker-arm:latest
```
5) Verify bot joins and responds to @YourBot ping
6) Run detatched
```
docker run -d -v /path/to/auth.json:/node_modules/AwesomeBot/auth.json \
-v /path/to/config.json:/node_modules/AwesomeBot/data/config.json \
-p 0.0.0.0:80:8080 \
--name your_container \
-t taylorsmcclure/abdocker-arm:latest
```
