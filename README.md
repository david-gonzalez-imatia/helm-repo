# ImPlatform Initializr Helm Charts repository

Create the following secret files with the tokens to access the code repositories and the bot account:

secret2.yaml

```sh
apiVersion: v1
kind: Secret
metadata:
  name: repo-secret2
type: kubernetes.io/basic-auth
stringData:
  username: repouser
  password: 55frtrtaiu54pfaeru34f345exampletoken
``` 

secret.yaml 

```sh
apiVersion: v1
kind: Secret
metadata:
  name: repo-secret
type: kubernetes.io/basic-auth
stringData:
  username: botuser
  password: 55frtrtaiu54pfaeru34f345exampletoken
``` 

Add the secrets to your Kubernetes cluster:

```sh
$ kubectl apply -f secret.yaml 
``` 
