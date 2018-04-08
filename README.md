# docker-dl
Dockerfile for DeepLearn (Mxnet , Pytorch , Caffe2 , Tensorflow). This repository recommends developers to use, which covers cuda9.1, cudnn7.0, tensorflow1.6, opencv3.4.1, pytorch0.3.1, mxnet1.1 ,caffe,caffe2 .

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

