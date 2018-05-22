# Node App

This is a Docker image for test. This image include a Node.JS application.


### Prerequisites

* Docker
* Curl
* NPM



### Installing

You will need clone this repository locally and build the image before test it.

```
$ docker build -t node.app .
```

After build you can run the image

```
docker run -p 49160:8080 -d node.app
```

## Running the tests

To test your app, get the port of your app that Docker mapped:

```
$ docker ps

# Example
ID            IMAGE                                COMMAND    ...   PORTS
ecce33b30ebf  node.app:latest  npm start  ...   49160->8080
```

Now you can call your app using curl (install if needed via: sudo apt-get install curl):

```
curl -i localhost:49160
```

After execute the curl command you will seee some like this:

```
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 12
ETag: W/"c-M6tWOb/Y57lesdjQuHeB1P/qTV0"
Date: Mon, 13 Nov 2017 20:53:59 GMT
Connection: keep-alive

Hello world
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details


