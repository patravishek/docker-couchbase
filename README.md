# Deploying Multiple Couchbase Server Containers on One Physical Machine
---

Run the following commands in terminal

```bash
docker run -d --name db1 couchbase
docker run -d --name db2 couchbase
docker run -d --name db3 -p 8091-8094:8091-8094 -p 11210:11210 couchbase
```
