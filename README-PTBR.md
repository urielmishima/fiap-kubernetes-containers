# MediaWiki on Kubernetes

Este projeto fornece uma implantação do MediaWiki em um cluster Kubernetes. O projeto usa um Deployment para implantar duas cópias de um contêiner MediaWiki. O Deployment também usa probes para garantir que os contêineres estejam em execução e prontos para receber solicitações. O Service expõe o Deployment para o mundo externo usando um LoadBalancer.

## Pré-requisitos

Para usar este projeto, você precisa ter o seguinte:

- Um cluster Kubernetes
- O kubectl CLI instalado e configurado para se conectar ao seu cluster

## Implantação

Para implantar este projeto, você pode usar o seguinte comando:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Para obter o endereço IP do balanceador de carga, você pode usar o seguinte comando:

```bash
kubectl get service mediawiki-service
```

O endereço IP do balanceador de carga é o valor listado para `EXTERNAL-IP`.

## Arquivos

- `deployment.yaml` - O arquivo de implantação que define o Deployment para o MediaWiki.
- `service.yaml` - O arquivo de serviço que define o Service que expõe o Deployment para o mundo externo.

## Configuração

Você pode configurar o projeto modificando os arquivos `deployment.yaml` e `service.yaml`. Por exemplo, você pode modificar o número de réplicas no Deployment ou o tipo de Serviço.

## Informações

* **Curso:** MBA em Cloud - Engineering & Architecture
* **Turma:** 2CLDR
* **Nome:** Uriel Mishima
* **RM:** 346005
* **Disciplina:** Orquestração Kubernetes e Containers
