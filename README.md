# get-api-group

we can use the client module to interact with the kubernetes resources. 

But In Python, we instantiate ApiextensionsApi class from client module:

`client_api = client.ApiextensionsApi()`         

Here I've created the client with it's respective class ApiextensionsApi
and storing in a var named as client_api. so furture we can use it.

`KubeConfig:` to pass the on local cluster e.g minikube we use bellowcommand: 

`config. load_kube_config()`

#### Authenticating to the Kubernetes API server

But what if you want to list all the api group of a GKE or any other  Cluster, you must need to authenticate the configuration

`configuration.api_key = {"authorization": "Bearer" + bearer_token}` 

I've used Bearer Token which enable requests to authenticate using an access key.

#### get the list of all api group:

call the function get_api_group(cluster_details)

And run following command:

`python3 get-api-group.py`

