*Clustering menggunakan Docker Swarm*

Pada Docker Swarm Cluster ini terdapat 2 bagian utama sebagai unsur yaitu, Swarm manager dan Swarm Worker. 

1. Swarm Manager memiliki tugas salah satunya membuat dan melakukan cluster service, selain itu swarm manager juga bertugas menyediakan HTTP API Endpoints. 
2. Swarm Worker bertugas untuk menjalankan container atau service yang telah di definisikan pada Swarm Manager.

-Pastikan serivce Docker daemon telah berjalan pada masing-masing host,cek menggunakan perintah : 
*/etc/init.d/docker status*
-Selanjutnya mulai menjalanan Swarm Clustering pada Host terlebih dahulu :
*docker swarm init --advertise-addr IP_Address*
-ganti IP_Address dengan ip address Host yang terhubung dengan VM, apabila menjalankan perintah tersebut pada sebuah host maka otomatis host tersebut menjadi Swarm Manager. Dari perintah diatas biasanya akan memperoleh output :
*Swarm initialized: current node (yybbhv38r19o4u2ws4of56e5c) is now a manager.
To add a worker to this swarm, run the following command:
docker swarm join \
–token SWMTKN-1-5frmgly6d0bo1nqkxs3ybz37d0drmrgfqj5u0l9maeuvr5pz8f-7kcknenqjk2insxo0ecmtwyfe \
IP_Address:2377
To add a manager to this swarm, run ‘docker swarm join-token manager’ and follow the instructions*
-Apabila Docker mengeluarkan output seperti diatas berarti telah berhasil menjalankan Swarm Cluster pada Swarm Manager. Setelah kita membuat Swarm Manager selanjutnya kita akan membuat Swarm Worker untuk join Swarm Manager. Jalankan perintah berikut pada VM yang telah disiapkan sebelumnya :
*docker swarm join \
--token SWMTKN-1-5frmgly6d0bo1nqkxs3ybz37d0drmrgfqj5u0l9maeuvr5pz8f-7kcknenqjk2insxo0ecmtwyfe \
IP_Address:2377*


