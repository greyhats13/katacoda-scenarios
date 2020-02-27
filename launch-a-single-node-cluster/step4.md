Aktifkan dashboard menggunakan Minikube dengan perintah minikube addons enable dashboard

Terapkan Kubernetes Dashboard dengan menggunakan definisi YAML berikut. Ini hanya bisa digunakan di Katacoda.

`kubectl apply -f /opt/kubernetes-dashboard.yaml`{{execute}}


Dashboard Kubernetes memungkinkan Kita melihat aplikasi dalam UI. Dalam deployment ini, dashboard telah tersedia di port 30000 tetapi mungkin perlu waktu untuk mulai menjalankannya.

Untuk melihat progres Dashboard, Lihat Pods dalam namespace kube-system menggunakan perintah
`kubectl get pods -n kubernetes-dashboard -w`{{execute}}

Setelah berjalan, berikut adalah URL dashboardnya https://[[HOST_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com/