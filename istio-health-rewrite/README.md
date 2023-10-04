# argo-example-apps
Example apps for argo cd

kubectl get pod liveness-http-669f7859d-mhggl -n istio-io-health-rewrite -o json | jq '.spec.containers[0].livenessProbe.httpGet'

kubectl get pod liveness-http-669f7859d-b9lnb -n istio-io-health-rewrite -o=jsonpath="{.spec.containers[1].env[?(@.name=='ISTIO_KUBE_APP_PROBERS')]}"
