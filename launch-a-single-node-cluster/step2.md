Cluster dapat berinteraksi dengan menggunakan kubectl CLI. Ini adalah pendekatan utama yang digunakan untuk mengelola Kubernetes dan aplikasi yang berjalan di atas cluster.

Rincian cluster dan status kesehatannya dapat dilihat dengan perintah `kubectl cluster-info`{{execute}}

Untuk melihat nodes di cluster gunakan perintah `kubectl get nodes`{{execute}}

Jika node ditandai sebagai NotRead, hal itu berarti node masih memproses komponen-komponennya.

Perintah ini menunjukkan semua node yang dapat digunakan untuk meng-host aplikasi kita. Sekarang kita hanya memiliki satu node, dan kita dapat melihat bahwa statusnya ready (siap menerima aplikasi untuk deployment).