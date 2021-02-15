# microservices-by-minikube

Source code updated to work without OpenShift and run in the Minikube Cluster accomplish with few modifications.

For use in development, the current model presents a vulnerability that does not follow good practices in the use of Kubernetes and so I developed this code model for the correct use of the creation of microservices in the Minikube.


[THE PROBLEM]

  ports:
    - protocol: 'TCP'
      port: 80
      targetPort: 8080
  >>> type: LoadBalancer
  
  The problem that occurred is a failure to create the backend microservice deployment that leaves a vulnerability in inter-pod communication where it will be corrected with a manual deployment using NodePort.
