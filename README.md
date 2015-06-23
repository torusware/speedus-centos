![speedus logo](http://dl.torusware.com/images/speedus_small.jpg "Torusware Speedus")
![centos logo](https://d207aa93qlcgug.cloudfront.net/1.79.3/img/explore_repos/official_centos.png "CentOS")
# Speedus Plug&Run Lite for CentOS
CentOS image with speedus solution for high-performance communications. Check us out at [our website](http://torusware.com/).

Speedus is your communications highway:

- Accelerates communications in the cloud and corporate IT systems
- Faster applications provide businesses with higher competitive advantages while reducing their IT bill
- 100% nonintrusive software solution which takes full advantage of the underlying hardware

#Supported tags and respective `Dockerfile` link
Each tag corresponds to the tag of the centOS base image:

- [`centos7`](https://github.com/torusware/speedus-centos/tree/master/centos7 "centos7 Dockerfile"), [`latest`](https://github.com/torusware/speedus-centos/tree/master/centos7 "latest Dockerfile")
- [`centos6`](https://github.com/torusware/speedus-centos/tree/master/centos6 "centos6 Dockerfile")

#Launching instructions
In order to run a container with our image, execute:

    sudo docker run -ti torusware/speedus-centos

This will launch a `bash` shell where you can execute whatever program you want.

In this image we provide a built-in communication tests, Netpipe. Just execute:

    NPtcp &
    NPtcp -h localhost

For getting the baseline. To perform the test with our solution:

    speedus NPtcp &
    speedus NPtcp -h localhost

As you can see, using speedus is really easy and non-intrusive, just type `speedus` before your application:

    speedus /path/to/the/program [parameters]

If you need more information, you can check the README file inside the container or contact us at <info@torusware.com>

#Check our other images in the Docker Hub

- [speedus-ubuntu image](https://registry.hub.docker.com/u/torusware/speedus-ubuntu/ "Speedus Plug&Run Lite for Ubuntu")
- [speedus-redis image](https://registry.hub.docker.com/u/torusware/speedus-redis/ "Speedus Plug&Run Lite for Redis")
- [speedus-mongo image](https://registry.hub.docker.com/u/torusware/speedus-mongo/ "Speedus Plug&Run Lite for MongoDB")

#Example Use Case

- [Optimizing communications between Docker containers](http://blog.torusware.com/2015/04/optimizing-communications-between.html "Optimizing communications between Docker containers")
- [Increasing performace of a MongoDB Docker container in Azure](http://blog.torusware.com/2015/05/increasing-performace-of-mongodb-docker.html "Increasing performace of a MongoDB Docker container in Azure")
