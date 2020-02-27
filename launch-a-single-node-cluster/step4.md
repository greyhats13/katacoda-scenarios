Enable the dashboard using Minikube with the command minikube addons enable dashboard

Make the Kubernetes Dashboard available by deploying the following YAML definition. This should only be used on Katacoda.

`kubectl apply -f /opt/kubernetes-dashboard.yaml`{{execute}}

The Kubernetes dashboard allows you to view your applications in a UI. In this deployment, the dashboard has been made available on port 30000 but may take a while to start.

To see the progress of the Dashboard starting, watch the Pods within the kube-system namespace using `kubectl get pods -n kubernetes-dashboard -w`{{execute}}

Once running, the URL to the dashboard is https://2886795287-30000-elsy05.environments.katacoda.com/