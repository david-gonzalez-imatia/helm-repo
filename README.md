# Test Helm Charts repository

In order to deploy the templates you must create a secret that includes the token or password to access git repositories:

```sh
apiVersion: v1
kind: Secret
metadata:
  name: repo-secret
type: kubernetes.io/basic-auth
stringData:
  username: user
  password: password
```  

Add the secret to the namespace you want with kubectl and configure the name of the secret in the values.yaml file in the chart.
