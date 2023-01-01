# docker-k8s-helm
Demo use : Docker, K8s, helm
# Docker CMD
  ```
docker ps

docker ps -a

docker images

docker inspect image_id*

docker logs id-container

docker logs -f id-container

docker stop container-id

docker start container1-id container1-id

docker container  pause container-id

docker kill id-container

docker stats
  ```

# Example this commande run docker keycloack 
  ```
docker run -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:20.0.2 start-dev
  ```
# Kubernetes CMD

  ```
kubectl apply -f filename.ml

kubectl get services / pod / deployment

kubectl set image deployment deployment-name service-name=new_image_version

kubectl describe pod accounts-deployment-6cfbcf6864-6zms9

kubectl get secret keycloak -o yaml => get  secret

kubectl get pods -w --namespace default => watch deployment
  ```
# HELM CMD

  ```
helm create staging/dev/prod => create template

helm ls

helm install dev-deployment dev

helm ls

helm upgrade dev-deployment dev-common

helm uninstall dev-deployment => uninstall deployment

helm dependency/dependencies build

helm history dev-deployment

helm rollback dev-deployment revision_number

helm repo add bitnami https://charts.bitnami.com/bitnami => add bitnami

helm install keycloak bitnami/keycloak => install from bitnami repos. 

helm install mysqldb --set auth.rootPassword=root,auth.database=mysqldb bitnami/mysql
  ```