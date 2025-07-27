this is a copy from cilium project

https://github.com/cilium/cilium/tree/main/examples/minikube


Tips to generate multiple xwing blocks
for i in {2..101}; do                                                                                                                                                               
cat <<EOF     
---      
apiVersion: v1
kind: Pod      
metadata:
  name: xwing$i                    
  labels:        
    app.kubernetes.io/name: xwing$i
    org: alliance
    class: xwing$i
spec:              
  containers:                                                                                                     
  - name: spaceship
    image: quay.io/cilium/json-mock:v1.3.8@sha256:5aad04835eda9025fe4561ad31be77fd55309af8158ca8663a72f6abb78c2603           