# hello-world

##Generating the hello-world image.
	>minikube start
	>eval $(minikube -p minikube docker-env)
	>docker build -t todvil/hello-world .
####The Dockerfile is used by the Docker engine to create a new Docker image of the application container. So make sure to be in the right directory when executing the docker build command.

##Deploying to Kubernetes service
	>kubectl apply -f deployment.yaml

##Verify that everything is created successfully
	>kubectl get deployments
	>kubectl get services
Or use the Minikube dashboard which can be accessed via
	>minikube dashboard

##To access the Hello World through your browser, execute the following:
	>kubectl port-forward svc/hello-world-service 8000:8000 &

##Go to your browser and open
	>127.0.0.1:8000

##To kill the process execute
	>pkill kubectl

