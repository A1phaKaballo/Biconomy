# Ping Pong API Whith Docker file and Kubernetes Deployment files 

### Steps to successfuly deploy the app and expose /ping API.
1- clone the project .<br /> 
2 cd to Biconomy/app.<br />
3- Run Docker Build Command to build and tag the image.<br />
4- upload the image to a private repository or docker hub.<br />
5- edit Biconomy/kube-manifists/deployment.yaml and change the image to your image URL.<br />
6- incase you uploaded the image to a repository you need to uncomment **imagePullSecrets:** and add a secret named biconomy to your cluster, it must include the credentials needed to login to the image repository.<br />
**Note:** to expose /ping only, we need to have an ingress controller, I am using custom controller, you need to edit Biconomy/kube-manifists/ingress.yaml and add **annonations** and **ingress class** that is suitable for your ingress controller .<br />
5- run " kubectl apply -f Biconomy/kube-manifists" to deploy the app to your kubernetes cluster
6- /ping shoud be now accessable through YOUR_INGRESS_CONTROLLER/ping 
