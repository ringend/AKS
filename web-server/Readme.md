
This is a webserver deployment for Azure AKS, with a public loadbalancer service.

The AKS instance this was run on was deployed via the portal as a "Basic" instance, using kubenet CNI.

It deploys the following dockerhub container:

**ringend/web-server2**

  Note:This container is listening on port 8080

The Azure loadbalancer is exporting port 80

**Example:**
spec:
  type: LoadBalancer
  ports:
  - name: http
  
    port: 80

    targetPort: 8080


