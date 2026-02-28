# Orquestração de Microsserviços com Docker 🐳

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org/)

Projeto de infraestrutura focado na orquestração de três microsserviços integrados, utilizando boas práticas de **DevSecOps** e **Containerização**.

---

## 🏗️ Arquitetura da Solução

O ambiente é composto por três camadas isoladas:
1.  **Frontend:** Servidor Nginx servindo uma interface estática.
2.  **API Saudação:** Microserviço Python para geração de mensagens.
3.  **API Pessoas:** Microserviço Python para gestão de dados aleatórios.

### Destaques de Engenharia (Shift Left Security)
- **Multi-stage Builds:** Dockerfiles otimizados para reduzir o tamanho das imagens e remover dependências de build do runtime.
- **Imagens Distroless/Slim:** Uso de `python:slim` e `nginx:alpine` para diminuir a superfície de ataque.
- **Isolamento de Redes:** Implementação de redes Docker específicas para controle de tráfego entre serviços (Backend vs Frontend).
- **Least Privilege:** Containers configurados para rodar com o mínimo de permissões necessárias.

---

## 🚀 Como Executar

### Pré-requisitos
- Docker >= 24.0
- Docker Compose >= 2.20

### Passo a Passo
1. Clone o repositório:
   ```bash
   git clone [https://github.com/jlima-cloud/desafio-docker-microsservicos.git](https://github.com/jlima-cloud/desafio-docker-microsservicos.git)
   cd desafio-docker-microsservicos