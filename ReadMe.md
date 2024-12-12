#Overwrite CMD Instruction
docker run --rm -d --name app1 --publish 8081:8080  sreeharshav/devsecopsb41:v6 --port 8080

docker run --rm -d --name fastap1 \
> -e AWS_ACCESS_KEY_ID=AKIA2QEFLENWA6Z4KDDT \
> -e AWS_SECRET_ACCESS_KEY=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 \
  -v /root:/rootdata \
> -p 80:80 sreeharshav/devsecopsb41:v1

#Build Arguments
docker build --build-arg T_VERSION="1.8.5"  -t sreeharshav/devsecopsb41:v2 -f Dockerfile.Dev .
