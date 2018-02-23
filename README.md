# docker-dl
Dockerfile for DeepLearn (Mxnet , Pytorch , Caffe2 , Tensorflow). This repository recommends developers to use, which covers cuda9.0, cudnn7.0, tensorflow1.5, opencv3.4, pytorch0.3, mxnet1.0 .

#### The docker registry is :
https://hub.docker.com/r/jermine/dl/

#### The Github repo is:
https://github.com/JermineHu/docker-dl

# Used
**You can switch the environments by docker images tags!**
#### Checked nvidia driver info 
```
docker run --runtime=nvidia --rm -it jermine/dl:tensorflow.gpu nvidia-smi
```
#### Get pip3 list
```
docker run --rm -it jermine/dl:tensorflow.gpu pip3 list --format=columns
```

