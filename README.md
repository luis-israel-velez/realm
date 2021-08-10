Testing various techniques to better my Web Development skills. 

The following was heavily influenced by: https://www.youtube.com/watch?v=u3sXfcncrJQ

1. First we create a small app using nodejs
   npm init
   Multiple .js files with code 
   npm install --Get dependencies inserted into a node_module directory as well as the _lock package
   setup scripts on the package.json to determine what to start
   Test it with npm run <script>
2. If step above is successful then now we need to "dockerize" 
   Create a Dockerfile on each section that we need an image
   FROM - define the base images 
   WORKDIR - define working directory (important for node that needs the modules) 
   COPY - copy the files from your project directory into the image 
   EXPOSE - Expose the port the image will use (and that need to be connected with host) 
   CMD - What will be executed
   Build the image with the following command "docker build . -f <dir> -t <name>:<version>

   Once you execute "docker run -d <detach> -p 3015:3015 <image>:<tag> you can see at Logs 
   docker logs <id of image> 


