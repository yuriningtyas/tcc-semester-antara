*Kubernetes*

Kubernetes adalah platform open source yang digunakan untuk manajemen container. Kubernetes bisa disingkat menjadi K8s dimana huruf K merupakan huruf depan, angka 8 merupakan jumlah huruf dari “ubernete” dan s adalah huruf terakhir. Sehingga Kubernetes = K8s .
Dengan menggunakan container, seluruh aplikasi yang kita miliki akan di kemas sehingga ketika akan di jalankan dimanapun, aplikasi tersebut akan berjalan sama serperti pada saat kita mencobanya, tidak perlu lagi menginstall server dengan berbagai macam aplikasi, environment, dan kebutuhan lainnya, karena semua yang dibutuhkan oleh aplikasi tersebut sudah terpasang di container.
Untuk menjalankan container, tentunya membutuhkan sebuah aplikasi. Aplikasi yang paling umum digunakan adalah Docker. Docker di install di server, kemudian kita jalankan docker image dan terbentuklah container dan aplikasi kita sudah berjalan dan bisa digunakan.
Tetapi untuk kebutuhan production, tidak cukup hanya sekedar aplikasi bisa berjalan, kita membutuhkan sistem yang handal yang mampu membuat aplikasi kita selalu available, tidak ada downtime, memiliki security yang handa, bisa menerima banyak traffic, dan sebagainya. Untuk itu diperlukan lah sebuah orkestrasi (orchestration) yang bertugas untuk memanajemen itu semua. Maka yang bisa kita gunakan untuk itu semua adalah kubernetes.


*Konsep Kubernetes*


-Cluster Kubernetes
Dalam Cluster Kubernetes terdapat beberapa node. Node merupakan Server, server fisik atau Virtual Private Server (VPS) yang digunakan untuk menjalankan kubernetes. Untuk membuat cluster kubernetes dibutuhkan setidaknya 1 server untuk kubernetes-master atau node-master dan 1 server untuk kubernetes-node atau node-1.
-Kubernetes Master
Kubernetes master adalah server yang bertindak sebagai node-master. Kubernetes master menjalankan tiga komponen yaitu kube-apiserver, kube-controller-manager, dan kube-scheduller.
-Kubernetes Nodes
Kubernetes nodes adalah semua server non-master yang terdaftar di server master. Kubernetes nodes menjalankan dua komponen, yaitu kubelet dan kube-proxy.

*Object kubernetes
1. Pod
2. Service
3. Volume
4. Namespace
