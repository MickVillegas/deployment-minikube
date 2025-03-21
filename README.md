# deployment-minikube

Definicion del deployment

![imagen](./img/1.png)

Inicio minikube con  

```
minikube start --driver none --network-plugin cni --cni flannel
```

![imagen](./img/c3.png)

Y creo el deployment con

```
kubectl  apply -f actDeploiment.yaml
```

![imagen](./img/2.png)

Comprobación de los recursos creados con  

```
kubectl  get all
```

![imagen](./img/c1.png)

Reviso por separado los recursos creados
- deployments

  ```
  kubectl get delpoyments 
  ```

- replicas

  ```
  kubectl get replicasets
  ```

- pods
 
  ```
  kubectl get pods 
  ```

![imagen](./img/4.png)

Informacion detallada del deployment con  

```
kubectl describe deployment.apps mi-deployment
```

![imagen](./img/5.png)

Informacion sobre los logs con  

```
kubectl logs deployments/mi-deployment
```

![imagen](./img/6.png)

Acceso desde un navegador web a la aplicación usando el port-forward y busco en el navegador la ip y el puerto

```
kubectl port-forward mi-deployment-b5d9986d7-8tsxc 8000:80 --address 0.0.0.0
```

![imagen](./img/b1.png)
![imagen](./img/c2.png)
