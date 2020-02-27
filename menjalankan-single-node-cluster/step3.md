Dengan Kubernetes cluster yang berjalan, container sekarang dapat digunakan.

Dengan kubectl run, akan memungkinkan containers dideploy kedalam cluster - `kubectl create deployment first-deployment --image=katacoda/docker-http-server`{{execute}}

Status deployment bisa dilihat melalui Pods yang berjalan - `kubectl get pods`{{execute}}

Setelah container jalan, container tersebut dapat diekspos melalui opsi networking yang berbeda, tergantung pada kebutuhan. Salah satunya adalah NodePort, yang menyediakan port dinamis ke sebuah container.

`kubectl expose deployment first-deployment --port=80 --type=NodePort`{{execute}}


Perintah di bawah ini akan mencari port yang dialokasikan dan mengeksekusi permintaan HTTP.
The command below finds the allocated port and executes a HTTP request.

`export PORT=$(kubectl get svc first-deployment -o go-template='{{range.spec.ports}}{{if .nodePort}}{{.nodePort}}{{"\n"}}{{end}}{{end}}')
echo "Accessing host01:$PORT"
curl host01:$PORT`{{execute}}

Hasilnya adalah container yang memproses permintaan.