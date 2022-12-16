# Docker storage


### Volumes

![image](https://user-images.githubusercontent.com/25337881/207859296-6c9746f5-5ef3-4d16-b13c-df729b56e447.png)


![image](https://user-images.githubusercontent.com/25337881/207859383-e6202dd1-08a6-4efc-8488-692ff7b79d0c.png)


### Command

```

## create volume with default location of image/volume/container (/var/lib/..)
docker volume create data_volume
docker run -v data_volume:/var/lib/mysql mysql

## mapping folder
docker run -v /opt/data:/var/lib/mysql mysql

## using mount
docker run --mount type=bind, source=/opt/data,tartget=/var/lib/mysql mysql


```
