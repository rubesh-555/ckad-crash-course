Create the namespace `rubesh` to begin with.
kubectl create ns rubesh
apply the below yaml
"""
       apiVersion: v1
        kind: Pod
        metadata:
          name: rate-limiter
          namespace: rubesh
        spec:
          containers:
          - name: business-app
            image: bmuschko/nodejs-business-app:1.0.0
            ports:
            - containerPort: 8080
        
          - name: ambassador
            image: bmuschko/nodejs-ambassador:1.0.0
            ports:
            - containerPort: 8081
        
          restartPolicy: Never
  """
          
kubectl apply -f rate-limiter.yaml

shell into the pod container using
kubectl exec rate-limiter -it -c rubesh -n rubesh -- /bin/sh



