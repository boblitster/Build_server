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
	
ANSIBLE 

	Sudo apt-get update

	sudo apt-get install -y libssl-dev libffi-dev python-dev python-pip 

	sudo pip install ansible
	
	
	
Create playbook
		
	nano docker-playbook.yml

Run playbook 

	ansible-playbook kubernetes-playbook.yml
	
You may have to run it directly from the bash command line

	./minikube.sh
