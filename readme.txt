Build:
docker build -t dockermq .

Run:
docker run --env LICENSE=accept --env MQ_APP_PASSWORD=passw0rd --env MQ_QMGR_NAME=QM1 --env MQ_TLS_KEYSTORE=/var/mqm/dockermq.p12 --env MQ_TLS_PASSPHRASE=dockermq --publish 1414:1414 --publish 9443:9443 --detach --name mq3 dockermq:latest