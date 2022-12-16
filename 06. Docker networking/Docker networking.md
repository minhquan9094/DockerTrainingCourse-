# 06. Docker networking


### Default networks


![image](https://user-images.githubusercontent.com/25337881/208015858-136777df-d471-4a96-bbb8-7586b72e3040.png)



### User-defined networks

```
## attach network to container
docker run -d --name=mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 --network wp-mysql-network mysql:5.6



## Create network
docker network create --driver bridge --subnet 192.168.100.0/24 --gateway 192.168.100.1 new-network-name

## verify setup
docker network ls

docker network inspect {name_network}


```

### Embedded DNS

We can using Name to connect between container in same network. DNS will be lookup from name to IP
