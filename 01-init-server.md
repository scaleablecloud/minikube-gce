* Login using key file
```
gcloud auth activate-service-account \
  devops@cobalt-poet-231218.iam.gserviceaccount.com \
          --key-file=key.json --project=cobalt-poet-231218
 ```
 
* SSH with compute engine vm instance
``` 
gcloud compute ssh gce-minikube
```

* Install important tools
```$xslt
sudo apt update
sudo apt -y install wget zip unzip file
sudo apt -y install git

```

