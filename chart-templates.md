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