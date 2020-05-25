# Deploying Multiple Couchbase Server Containers on One Physical Machine

Run the following commands in terminal

```bash
docker run -d --name db1 couchbase
docker run -d --name db2 couchbase
docker run -d --name db3 -p 8091-8094:8091-8094 -p 11210:11210 couchbase
```

Check the Docker logs to verify that the containers have started:

```bash
docker logs db1
docker logs db2
docker logs db3
``

If the containers have started, all the above commands should return the following output:

```bash
`Starting Couchbase Server -- Web UI available at http://<ip>:8091`
```
