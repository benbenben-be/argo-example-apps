# Used for testing argo cd / k8 hpa

Run the following
kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10

Run the load test
kubectl run -i --tty load-generator --rm --image=busybox:1.28 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"