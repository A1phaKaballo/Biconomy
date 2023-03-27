# Ping Pong API Whith Doker file and Kubernetes Deployment files 

### Steps to successfuly deploy the app and expose /ping API.
1- clone the project.<br /> 
2 cd to Biconomy/app.<br />
3- Run Docker Build Command to build and tag the imag.e.<br />
4- upload the image to a private repository or docker hub.<br />
5- edit Biconomy/kube-manifists/deployment.yaml and change the image to your image URL.<br />
6- Edit the host on Biconomy/kube-manifists/ingress.yaml to your own host.<br />
Note: to expose /ping only we need to have an ingress controller, I am assuming that you are running nginx ingress controller, Other ingress controllers require diferent configurations.<br />
### 5- run " kubectl apply -f Biconomy/kube-manifists" to deploy the app to your kubernetes cluster
### 6- /ping shoud be now accessable through YOUR_OWN_HOST/ping 

