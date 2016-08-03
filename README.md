# parse-docker

A docker container that runs [parse-server](https://github.com/ParsePlatform/parse-server) and [parse-dashboard](https://github.com/ParsePlatform/parse-dashboard)

## Build it

`docker build -t parse-docker .`

## Run it

`docker run -d -p 8080:8080 -p 9000:9000 -p 27017:27017 parse-docker`

## Open the dashboard

`open https://0.0.0.0:9000/` or `open https://<IP_HOST>:9000/`

The default username/password is "username" and "password". These can be set using environment variables in [Dockerfile](https://github.com/getsetgames/parse-docker/blob/master/Dockerfile).

## Run a Parse function

`curl -k -X POST -H "X-Parse-Application-Id: myAppId" -H "X-Parse-REST-API-Key: myMasterKey" -H "Content-Type: application/json" https://localhost/parse/functions/hello`
