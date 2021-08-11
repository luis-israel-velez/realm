Testing various techniques to better my Web Development skills. 

The following was heavily influenced by: https://www.youtube.com/watch?v=u3sXfcncrJQ

1.  First we create a small app using nodejs
    npm init
    Multiple .js files with code 
    npm install --Get dependencies inserted into a node_module directory as well as the _lock package
    setup scripts on the package.json to determine what to start
    Test it with npm run <script>
2.  If step above is successful then now we need to "dockerize" 
    Create a Dockerfile on each section that we need an image
    FROM - define the base images 
    WORKDIR - define working directory (important for node that needs the modules) 
    COPY - copy the files from your project directory into the image 
    EXPOSE - Expose the port the image will use (and that need to be connected with host) 
    CMD - What will be executed
    Build the image with the following command "docker build . -f <dir> -t <name>:<version>

    Once you execute "docker run -d <detach> -p 3015:3015 <image>:<tag> you can see at Logs 
    docker logs <id of image> 
3.  Now we start getting into kubernetes!! Start minikube with "minikube start --driver=docker"
4.  Build .yaml for deployment and run, make sure your docker is tied to the minikube docker
5.  Build .yaml for services both as ClusterIP (internal) or LoadBalancer (external)
6.  kubectl apply -f <filename> -- Get the deployment/service yaml executed and into the cluster. 
7.  Learn about the importance of commands like kubectl get pods/services. 
8.  Once we are done, let's jump into HELM. Build a helm chart and a value.yaml field with all other 
    components on the templates directory.
9.  Clean minikube cluster with kubectl delete deployments/services --all 
10. Execute helm install <dir> --generate-name 



Tools:
1. docker   (images, local repository)
2. kubectl 
3. minikube (driver=docker)

Setting: 
1.  eval $(minikube docker-env) -- Sets up the minikube docker repo, the following commands
    reverts that eval "$(docker-machine env -u)"


 

