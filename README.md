# thelounge-istio-k8s
Kubernetes + Istio deployment scripts for thelounge.chat IRC client

    kubectl apply -f *.k8s.yaml
    
Note: egress traffic is restricted to tls://chat.freenode.net:6697 
