- Necessário ter o terraform na máquina;
- Criar o arquivo terraform.tfvars e colocar os valores:

do_token      = SEU TOKEN DA DIGITALOCEAN
ssh_keys_name = SEU SSH DA DIGITALOCEAN
region        = REGIÃO PRETENDIDA PARA SUBIR AS MÁQUINAS

- Criar todo cluster utilizando o comando: terraform init e terraform apply;
- Após subir todas as máquinas;
- Realizar a cópia do arquivo kube_config.yaml :

cp .\kube_config.yaml C:\Users\SEU-USUARIO\.kube\config

- Ir na pasta /kube-news/k8s/ e aplicar o comando:

kubectl apply -f .\deployment.yaml

-  Checando o serviço:

![image](https://user-images.githubusercontent.com/6171256/215341000-561a8a89-be2a-494b-a128-b3b50453a034.png)

- Checando os pods:
![image](https://user-images.githubusercontent.com/6171256/215341058-c1f84a8d-56d1-4fd6-8999-b047d4f17564.png)

- Checando com get all:

![image](https://user-images.githubusercontent.com/6171256/215341087-1b40febe-8df6-490f-9c9c-3324aec5174f.png)

- Agora é aguardar o serviço receber um IP External. Note que na imagem da checagem anterior, está como <pending>
- Após alguns minutos, receberá um IP:
  ![image](https://user-images.githubusercontent.com/6171256/215341168-b11dba52-d324-4505-bdf0-600cebf35503.png)

  - Copie o IP, cole no navegador e utilize a aplicação:
  ![image](https://user-images.githubusercontent.com/6171256/215341224-09762ce1-a8ce-4485-968c-f05617f2fe44.png)
