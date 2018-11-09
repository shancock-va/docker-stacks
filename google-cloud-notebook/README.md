# Google Cloud Notebook

This docker container set's up what you need in order to run a Jupyter Notebook as a docker container that works well with Google Cloud.

## Get Started

### Checkout Docker Stacks
Checkout the parent repo that you are already looking in (https://github.com/shancock-va/docker-stacks).

### Building Your Docker Container
From the docker stacks direct you just checkouted run the following command

`docker build google-cloud-notebook -t google-cloud-notebook -f google-cloud-notebook/Dockerfile`

This command may take a while depending on whether or not you have the proper docker images already. If you don't they will be downloaded for you.


### Start Jupyter Notebook
From the docker stacks direct you just checkouted run the following command

`docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v ~/githup/bizops-datalab:/home/jovyan/work google-cloud-notebook`