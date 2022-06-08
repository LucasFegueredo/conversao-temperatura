Projeto do curso de Docker / Kubernets

Para criação e utilização da imagem, dentro da pasta ./src digite os seguintes comandos: 

• docker build -t conversao-temperatura:v1 .

• docker run -d -p 8080:8080 conversao-temperatura:v1

===============================================================================================================

Para utilizar um kubertes faça a instalação do k3d e do kubectl.

Instalar K3D: • https://k3d.io/

Instalar Kubectl: • https://kubernetes.io/docs/tasks/tools/

Na pasta ./k8s faça o seguinte:

• k3d cluster create cluster-conv-temp --agents 3 --servers 3 -p "8080:30001@loadbalancer"

• kubectl apply -f deployment.yaml

Para testar, acesse: http://localhost:8080
