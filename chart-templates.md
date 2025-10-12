# CLI 
generates final template what would be deployed
- helm template infrastructure/nginx
Lint check
- helm lint infrastructure/nginx 
install
- helm install local-nginx infrastructure/nginx # release name / path to chart
package in .tar
- helm package infrastructure/nginx
install from .tar
- helm install local-nginx infrastructure/nginx-0.1.0.tgz
create index yaml
- helm repo index .
push to repo helm-charts-repo
- helm repo index . --url https://lenny606.github.io/helm-charts-repo/index.yaml
add repo
- helm repo add my-helm-charts https://lenny606.github.io/helm-charts-repo/