Aplicação de posts KubeDevNews rodando em k8s

#Subir o cluster:
k3d cluster delete meucluster -p "80:30000@loadbalancer"

#Após isso, ir na pasta srv e subir a aplicação:
kubectl apply -f .\deployment.yaml

#Aplicação rodando:
![image](https://user-images.githubusercontent.com/6171256/215295107-75a364b0-8365-4f51-b508-b2c61cfe09c6.png)
