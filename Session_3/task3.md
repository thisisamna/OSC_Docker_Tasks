# Docker Session 3 Task

## Q1

```
docker run -itd  --name db1 -e POSTGRES_PASSWORD=pass1234 -v db1Volume:/var/lib/postgres/data --network host --memory 500MB postgres
```

OR

```
mkdir /home/amna/db1Volume
docker run -itd  --name db1 -e POSTGRES_PASSWORD=pass1234 --mount type='bind',source=/home/amna/db1Volume/,target=/var/lib/postgres/data  --network host --memory 500MB postgres
```

## Q2

c1 and c2

```
docker network create oneandtwo
docker run -itd --name c1 --network oneandtwo alpine
docker run -itd --name c2 --network oneandtwo alpine

# check connectivity
docker attach c1
ping c2
```

c3 and c4

```
docker run -itd --name c3 alpine
docker run -itd --name c4  alpine

# check connectivity
docker inspect c4
# ip address is 172.17.0.3
docker attach c3
ping 172.17.0.3
```

## Q3

[Screenshot](Q3.png)

## Q4

- db1 : " " (Empty because it is the same as the host)

- c1: 172.18.0.2

- c2 : 172.18.0.3

- c3: 172.17.0.2

- c4: 172.17.0.3
