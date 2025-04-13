 Here we are using minikube[which provides single node by default].
 Minikube runs your Kubernetes cluster inside a local VM or container (like on VirtualBox, Docker, etc.), and this VM uses a private IP (like 192.168.x.x) that's not accessible from the outside world — including:

Other machines

Your browser (unless it’s on the same host)

EC2 public IPs

So, when you create a NodePort or even a LoadBalancer service in Minikube:

The NodePort works only inside Minikube’s network, not your host or cloud EC2 network.

LoadBalancer shows <pending>, because Minikube doesn’t actually have a cloud load balancer (like AWS ELB) to assign a public IP.

Why we didnt used any build tool, beacause pyton is an Interpreted language no need of any build tools whereas java is not an interpreted language it should be compiled before running.
