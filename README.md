# MINIKUBE
# STEPS TO INSTALL MINIKUBE:-

In order to install minikube, there are some prerequisites given below:-

• Pre-Install Ubuntu 22.04 system

• 2 GB RAM or more

• 2 CPU or more

• 20 GB free disk space

**STEP-1**To download and install minikube binary, run following commands,


```$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64```

```$ sudo install minikube-linux-amd64 /usr/local/bin/minikube```

**STEP-2** To verify the minikube version, run

```$ minikube version```


![image](https://github.com/user-attachments/assets/56d5e70f-1a73-466b-a8df-f4d542896565)


**STEP-3** Install Kubectl tool:-
Kubectl is a command line tool, used to interact with your Kubernetes cluster. 
So, to install kubectl run beneath curl command->

```$ curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl```

**STEP-4** set the executable permission on it and move to /usr/local/bin:-

```$ chmod +x kubectl```

```$ sudo mv kubectl``` 

```/usr/local/bin/``` 

**STEP-5** Verify the kubectl version, run

```$  kubectl version -o yaml```


![image](https://github.com/user-attachments/assets/8709c13c-e23a-487b-846f-2939aae5680f)


# Start Minikube Cluster
**STEP-6** Now that Minikube is installed, start a Kubernetes cluster using the following command:

```$ minikube start--driver=docker```


![image](https://github.com/user-attachments/assets/acaebd0c-cc9f-4dbf-bb27-ebece02e1b30)



This command initializes a single-node Kubernetes cluster, and it might take a few minutes to download the necessary components.

**STEP-7** Once the minikube has started, verify the status of your cluster, run

```$minikube status```

**STEP-8** Use kubectl to interact with your Minikube Kubernetes cluster. For example, you can check the nodes in your cluster:


```$ kubectl get nodes```
```$ kubectl cluster-info```

**STEP-9** To deploy a sample nginx deployment, run following set of commands.

```$ kubectl create deployment nginx-web --image=nginx```

```$ kubectl expose deployment nginx-web --type NodePort --port=80```

```$ kubectl get deployment,pod,svc```

**STEP-10** To enable the more funtionality with addons or to view all the available addons, run:-


```$ minikube addons list```


![image](https://github.com/user-attachments/assets/f079dc03-6684-4b99-94d6-56dde3c824ff)



```$ minikube addons enable dashboard```

```$ minikube addons enable ingress```

**STEP-11** To start the Kubernetes dashboard run below command, it will automatically launch the dashboard in the web browser as shown below:-

```$ minikube dashboard```



![image](https://github.com/user-attachments/assets/9edecd03-b7fe-4c2b-804a-4e0f9e059596)


![image](https://github.com/user-attachments/assets/8b348cfa-12ce-451f-a9fe-3ed933a2aaa8)




