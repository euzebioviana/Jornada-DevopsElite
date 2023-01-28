# Projeto conversão de temperatura

### Sobre o projeto
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS. O projeto tem como objetivo ser um exemplo para a criação de ambiente com containers usando NodeJS.

### Observações do projeto
A aplicação é exposta usando a porta 8080

### Rodando em k8s

#Subir o cluster:
k3d cluster create meuclusterConvert -p "8080:30003@loadbalancer"

#Após isso ir até a pasta k8s e subir a aplicação:
kubectl apply -f .\deployment.yaml

#Pods em execução:

![image](https://user-images.githubusercontent.com/6171256/215294921-76404af7-7311-4627-9e20-cc5e31da02f2.png)
