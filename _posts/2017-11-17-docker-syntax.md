---
layout: post
title:  "Test Blog Docker"
image: "http://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/02/1424055625jekyll.png"
date:   2016-03-21
excerpt: "Simple Jekyll theme for your blog by Alperen Bozkurt."
project: true
tag:
- jekyll
- JBlog
- blog
- about
- theme
---




### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version}
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```
