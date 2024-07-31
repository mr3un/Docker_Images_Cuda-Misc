# Docker_Images_Cuda-Misc

This is linked to https://hub.docker.com/repository/docker/3uun/cuda_with_misc/general.

Have you ever run into situation that your ubuntu's nv drive/cuda version was not matched to whatever ML framework you just see on twitter? For example you installed the latest 555 driver with cuda 12.5 pre-install but found that it is mission impossible to downgrade your driver/cuda to whatever requirment due to NV driver quickness? 

Docker may save you from those problem! The idea is that to create container with different cuda verision so you can switch between those enviorment whatever you need. Here i create a two docker images with cuda 12.1 and 11.8 with some ML necessary package (conda, notebook, torch, pandas, numpy, scipy) for your convenience.

All you have to deploy these enviorment is to install nvidia-docker (https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) and then: 

docker pull 3uun/cuda_with_misc:12.1 

or 

docker pull 3uun/cuda_with_misc:11.8

These two images was based on nvidia official 12.1.0-runtime-ubuntu22.04 and 11.8.0-cudnn8-devel-ubuntu18.04. 
###Note your base system NV driver/cuda need to be higher or equal to whatever docker image you use. 

####to do: provide a way to automatically create those image without pulling 20g from dockerhub.
