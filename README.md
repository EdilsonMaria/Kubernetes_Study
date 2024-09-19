# Aplicação Front-End com Nginx e MySQL no Kubernetes

Este repositório contém um exemplo de implantação de uma aplicação front-end utilizando Nginx e um banco de dados MySQL no Kubernetes. O ambiente será configurado utilizando o Minikube, que permite executar um cluster Kubernetes localmente.

## Pré-requisitos

Antes de começar, verifique se você tem os seguintes requisitos instalados:

- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

## Estrutura do Projeto

O projeto contém os seguintes arquivos de configuração Kubernetes:

- `nginx-deployment.yaml`: Define o Deployment para o Nginx.
- `mysql-deployment.yaml`: Define o Deployment para o MySQL.
- `service.yaml`: Define os Services para expor os pods.

## Passos para Criar e Iniciar a Aplicação

1. **Inicie o Minikube:**

   Abra seu terminal e inicie o Minikube com o seguinte comando:

   ```bash
   $ minikube start

2. **Aplique os arquivos de configuração do Kubernetes**

    ```bash
    $ kubectl apply -f mysql-deployment.yaml
    $ kubectl apply -f nginx-deployment.yaml
    $ kubectl apply -f service.yaml

3. **Verifique se os Pods estão em execução:**

    ```bash
    $ kubectl get pods

4. **Verifique se os Services estão em execução**

    ```bash
    $ kubectl get services

5. **Para parar e remover os Deployments e Services criados, execute:**

    ```bash
    $ kubectl delete -f mysql-deployment.yaml
    $ kubectl delete -f nginx-deployment.yaml
    $ kubectl delete -f service.yaml

6. **Quando terminar, você pode parar o Minikube com o seguinte comando:**

    ```bash
    $ minikube stop
    $ minikube delete

### Explicação:

- **Pré-requisitos:** Lista as ferramentas necessárias para seguir o guia.
- **Estrutura do Projeto:** Explica os arquivos de configuração Kubernetes incluídos no projeto.
- **Passos para Criar e Iniciar a Aplicação:** Detalha como configurar e executar a aplicação no Minikube.
- **Estrutura dos Arquivos de Configuração:** Inclui exemplos de YAML para MySQL, Nginx e Services.
- **Parar e Remover a Aplicação:** Instruções para limpar os recursos criados.
- **Contribuições e Licença:** Informações sobre como contribuir e a licença do projeto.

Este `README.md` fornece uma documentação clara e abrangente sobre como configurar e executar uma aplicação front-end com Nginx e MySQL usando Kubernetes no Minikube. Você pode personalizar conforme necessário.


