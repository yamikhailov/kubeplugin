# kubeplugin
A kubectl monitoring plugin written in bash. 

## Requirements
Monitoring server needs to be installed and enabled as addon in case you are using tools such as minikube.
To install metrics server run:
```bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

## Installation
To install the following script as a kubectl plugin add the path to $PATH env variable and add ```kubectl-``` prefix to the file

```bash
sudo cp kubeplugin /usr/bin/kubectl-kp
```

## Usage
List all installed plugins and make sure that plugin is installed correctly

```bash
kubectl plugin list
```

Run the plugin with the following commands

```bash
kubectl kp pod
kubectl kp node
```