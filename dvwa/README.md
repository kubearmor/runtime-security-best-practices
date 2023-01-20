# DVWA Runtime Security Best Practices

1. Create new namespace for installing dvwa: `kubectl create ns dvwa`
1. Install DVWA application: `kubectl apply -f https://raw.githubusercontent.com/nyrahul/src/master/dvwa/dvwa-deploy.yaml -n dvwa`
1. Install karmor cli tool: `curl -sfL http://get.kubearmor.io/ | sudo sh -s -- -b /usr/local/bin`

## Application Hardening
1. Get recommended policies for dvwa app: `karmor recommend -n dvwa`
1. Get behavioural policies for dvwa app: `karmor discover -n dvwa`
1. Get network segmentation policies for dvwa app: `karmor discover -n dvwa -p NetworkPolicy`

