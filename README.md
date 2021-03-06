MG-RASTv4
=========

A rich Java script frontend for the v4 version of MG-RAST.


## Installation with Docker ##

To build this image:

make sure you have cloned the required repositories (including git submodules)

```bash
git clone --recursive https://github.com/MG-RAST/MG-RASTv4.git
```

To build the image either download the Docker file into an empty directory of provide the url to Dockerfile as in this example:

```bash
export TAG=`date +"%Y%m%d.%H%M"`
git clone --recursive https://github.com/MG-RAST/MG-RASTv4.git
cd MG-RASTv4
docker build -t mgrast/v4-web:${TAG} .
skycore push mgrast/v4-web:${TAG}
```

Example for manual invocation:
```bash
docker run -ti -p80:80 --name mgrast-v4-web mgrast/v4-web
```

Once that is done, connect to localhost on your machine with your favorite browser. (http://127.0.0.1)

### Other notes ###


location of html pages: /usr/share/nginx/html/

The dockerfile allows building a slim container with alpline base or a fatter one with nginx (debian base). Just look at the Dockerfile

