# CISO-assistant
Installation
Add the repository
helm repo add intuitem https://intuitem.github.io/ca-helm-chart/
Pulling default values
helm show values intuitem/ciso-assistant > my-values.yaml
Creating a dedicated namespace
kubectl create ns ciso-assistant
Install
helm install polpo intuitem/ciso-assistant -f my-values.yaml -n ciso-assistant
Uninstall
helm uninstall polpo -n ciso-assistant
Upgrading
When upgrading, make sure to:

Backup your persistent volumes
Update any custom values
Run: helm upgrade my-release . --set global.appVersion=vx.y.z
