docker build -t feedback-node:1 .
docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback  feedback-node:1
named volume name feedback a za : je path inside container

docker volume ls
http://localhost:3000/feedback/awesome.txt


Now you just start piling up a bunch of unused anonymous volumes - you can clear them via docker volume rm VOL_NAME or docker volume prune.