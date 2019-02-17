```$xslt
gcloud compute disks create disk1 --image-project debian-cloud --image-family debian-9
```

```$xslt
gcloud compute images create nested-vm-image \
  --source-disk disk1 --source-disk-zone us-east1-b  \
  --licenses "https://www.googleapis.com/compute/v1/projects/vm-options/global/licenses/enable-vmx"
```


```$xslt
gcloud compute instances create gce-minikube-helix --zone us-east1-b \
              --image nested-vm-image
```

```$xslt
gcloud compute ssh gce-minikube-helix
```

```$xslt
grep -cw vmx /proc/cpuinfo
```

