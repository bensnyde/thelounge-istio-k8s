# thelounge-istio-k8s
Kubernetes + Istio deployment scripts for thelounge.chat IRC client

### Credentials
The default credentials are:
* username: test
* password: test

You can overwrite either by modifying the irc.k8s.yaml Deployment *command*.

### Traffic
All traffic to and from the the application container is ran through an Envoy proxy courtesy of Istio. 

* Ingress traffic is currently wide-open, expose the port with:

    kubectl -n istio-system port-forward --address 0.0.0.0 service/istio-ingressgateway 8888:80

* Egress traffic is currently restricted to tls://chat.freenode.net:6697 

### Application: 
    kubectl apply -f *.k8s.yaml
    
