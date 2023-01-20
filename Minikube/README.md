# Overview

The Argo CD application is deployed automatically on Minikube. Use the following commands to use Argo Web UI.

1. Use `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo` command to get the **admin** password.
2. Use `kubectl port-forward svc/argocd-server --address 0.0.0.0 -n argocd 8080:443` command to expose Argo server.
3. In the browser go to **192.168.44.45:8080** and log in using credentials: username: `admin`, password: use password from the 1. step
