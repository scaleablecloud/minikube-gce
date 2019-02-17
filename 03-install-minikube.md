* Login using key file
```
gcloud auth activate-service-account \
  devops@cobalt-poet-231218.iam.gserviceaccount.com \
          --key-file=key.json --project=cobalt-poet-231218
 ```
 
* SSH with compute engine vm instance
``` 
gcloud compute ssh   gce-minikube
```

* Install Minikube on Linux by downloading a static binary

```$xslt
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
  && chmod +x minikube
```
* Add the Minikube executable to your path

```$xslt
sudo cp minikube /usr/local/bin && rm minikube
```

```$xslt
minikube start
```

# Install kubectl
```$xslt
sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo touch /etc/apt/sources.list.d/kubernetes.list 
echo "deb http://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```

# Install kubens
```$xslt
sudo git clone https://github.com/ahmetb/kubectx /opt/kubectx
sudo ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx
sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens
```