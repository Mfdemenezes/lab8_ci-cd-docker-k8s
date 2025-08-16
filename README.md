# lab8_ci-cd-docker-k8s

Objetivo: CI/CD com GitHub Actions: build & push (Docker Hub) + deploy via kubectl para K8s.

Adicionar no ci-cd-docker-k8s/README.md:

flowchart LR
    Dev((Commit)) --> Actions[GitHub Actions]
    Actions --> Build[Docker build]
    Build --> Hub[(Docker Hub)]
    Actions --> Deploy[kubectl apply]
    Hub --> Cluster[(Kubernetes)]
    Deploy --> Cluster
    Cluster --> Service[Service]
    User((Usuário)) --> Service
