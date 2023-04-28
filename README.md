Rclone Trials
=============

A basic setup for experimenting with Rclone and how it works with HDFS.

First, start up HDFS:

```
docker compose up -d hadoop
```

Once that's running, you should be able to list the contents of HDFS using:

```
docker compose run -ti rclone rclone ls h3:
```

Now you can run the trials scripts as defined in `docker-compose.yml`, using

```
docker compose run rclone
```

The `trials/copy-check-move.sh` script will create a test file, and then upload it to the Hadoop service.

