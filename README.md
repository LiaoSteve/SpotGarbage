SpotGarbage :Smartphone App to Detect Garbage Using Deep Learning
----------------------------------------------------
### Docker image [(https://github.com/kyamagu/caffe-docker)](https://github.com/kyamagu/caffe-docker)
* Run docker image in Windows, and share jupyter port to HOST.
```
docker run -it -v D:/docker_images/steve_caffe:/home/user -p 8888:8888 kyamagu/caffe
```
* Open terminal:
```
pip install opencv-python==3.1.0.0
```
## How to manage docker containers

To stop the running container,

```
docker ps
```

Check the container ID, and use `docker stop` command.

```
docker stop <Container-ID>
```

To restart the stopped container,

```
docker restart <Container-ID>
```

To list all the existing containers,

```
docker ps -a
```

To remove the container,

```bash
docker rm <Container-ID>
```

To remove the images, 
```
docker images
docker rmi <image>
```
## Description
* The **SpotGarbage_GarbNet** folder contains the caffe model related files for **GarbNet**.
* The code to test GarbNet is given in files named **garbnet_demo** in HTML, standard Python and Jupyter Ipython Notebook formats.
* The code requires the following dependencies installed:
  * Caffe (CPU or GPU)
  * OpenCV
  * PIL
  * Numpy

## Instructions
* Put the images on which garbage needs to be detected in the **input** folder.
* Run the **garbnet_demo.py** or run the code snippets through the Ipython notebook.
* The predictions will be made and the images with garbage regions segmented will be saved in the **output** folder.



