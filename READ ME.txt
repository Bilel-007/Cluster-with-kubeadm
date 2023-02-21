!! To use this files and this configurations you should have this tools installed on your local machine:
    -ansible.
    -vagrant.
    -virtualbox.

#use this command in the terminal of this folder to run the VMs:
$ vagrant up
#Upon completion, the Kubernetes cluster should be up and running. We can login to the master or worker nodes using Vagrant as follows:
$ ## Accessing master
$ vagrant ssh k8s-master
vagrant@k8s-master:~$ kubectl get nodes
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   18m     v1.13.3
node-1       Ready    <none>   12m     v1.13.3
node-2       Ready    <none>   6m22s   v1.13.3

$ ## Accessing nodes
$ vagrant ssh node-1
$ vagrant ssh node-2


if your virtualbox doesn't tolerate such range of Ip networks:
create a file : ' /etc/vbox/networks.conf '
paste this content in that text file : "    * 0.0.0.0/0 ::/0   " !! the * is important to copy.
