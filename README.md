# build_server

Create an image of of the files and send it to dockerhub

Sign into docker hub

Docker login  (boblitster & ***********)

Create environment variable 

export  DOCKERID=boblitster

echo $DOCKERID 

Create docker image


	docker image build --tag $DOCKERID/build_server:latest .


Run container using your new image 

	docker container run --detach --publish 80:80 --name build_server $DOCKERID/build_server:latest 

Push image to DockerHub 

	docker image push $DOCKERID/build_server:latest
