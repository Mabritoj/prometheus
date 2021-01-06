Within this repo, you will find a Kubernetes file to spin up Kube-State-Metrics on ARM (Raspberry Pi) and then Prometheus. Before the Kubernetes yaml file can be ran, a few things need to happen first:
1. Pull an ARM image of Kube-State-Metrics
  - docker pull carlosedp/kube-state-metrics:v1.9.6
2. Pull the latest Prometheus container
  - docker pull prom/prometheus
3. Tag and push both images to local Docker repository
4. Change the group owner on the volume mount to "nobody"
  - sudo chgrp -R nogroup /mnt/kubeshare/prometheus-store/
