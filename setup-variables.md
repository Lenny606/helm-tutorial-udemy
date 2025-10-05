# CLI 
path  to var has to be full from yaml

- helm install my-grafana grafana/grafana --version 10.0.0 --set "adminPassword=XXX" \
--set "adminUser=XXX"

# YAML

- kubectl create secret generic custom-grafana-credentials \
  --from-literal=admin-user=yyy \
  --from-literal=admin-password=yyy
- kubectl delete secret custom-grafana-credentials
add files to install
- helm install my-grafana grafana/grafana -f values/custom-values.yaml