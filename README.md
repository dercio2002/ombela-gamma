# ombela-gamma
Clone do Ombela Market - Projeto de Engenharia de Software
# Ombela Market

[![Java Version](https://img.shields.io/badge/Java-17-blue)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green)](https://spring.io/projects/spring-boot)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

> Marketplace digital focado na região centro-sul de Angola, promovendo inclusão digital e comércio regional.

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Arquitetura](#arquitetura)
- [Tecnologias](#tecnologias)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Testes](#testes)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Sobre o Projeto

### Visão
O Ombela Market é uma plataforma de marketplace e serviço de entregas que conecta vendedores locais de alta qualidade a clientes na região centro-sul de Angola.

### Objetivos
- Promover a inclusão digital de pequenos comerciantes
- Facilitar o acesso a produtos locais de qualidade
- Garantir segurança nas transações online

## Funcionalidades

| Funcionalidade | Descrição | Prioridade |
|----------------|-----------|------------|
| Autenticação | Cadastro, login, recuperação de senha | Must Have |
| Gestão de Produtos | CRUD de produtos com imagens | Must Have |
| Catálogo | Listagem, busca e filtros | Must Have |
| Carrinho | Adicionar/remover itens | Must Have |
| Checkout | Processamento de pagamentos | Should Have |
| Notificações | Alertas por email/SMS | Should Have |

## Arquitetura
## Tecnologias

### Backend
- **Linguagem:** Java 17
- **Framework:** Spring Boot 3.x
- **ORM:** Hibernate / JPA
- **Base de Dados:** MySQL 8.0
- **Build:** Maven

### Frontend
- **Framework:** React.js / Vue.js
- **Styling:** Tailwind CSS
- **State Management:** Redux / Pinia

### DevOps
- **Containerização:** Docker
- **CI/CD:** GitHub Actions
- **Versionamento:** Git

## Pré-requisitos

- JDK 17+
- Node.js 18+
- MySQL 8.0
- Docker (opcional)

## Instalação

```bash
# Clonar o repositório
git clone https://github.com/equipa-gamma/ombela-market.git
cd ombela-market

# Instalar dependências do backend
cd backend
./mvnw clean install

# Instalar dependências do frontend
cd ../frontend
npm install

# Executar a aplicação
docker-compose up -d

## Tecnologias

### Backend
- **Linguagem:** Java 17
- **Framework:** Spring Boot 3.x
- **ORM:** Hibernate / JPA
- **Base de Dados:** MySQL 8.0
- **Build:** Maven

### Frontend
- **Framework:** React.js / Vue.js
- **Styling:** Tailwind CSS
- **State Management:** Redux / Pinia

### DevOps
- **Containerização:** Docker
- **CI/CD:** GitHub Actions
- **Versionamento:** Git

## Pré-requisitos

- JDK 17+
- Node.js 18+
- MySQL 8.0
- Docker (opcional)

## Instalação

```bash
# Clonar o repositório
git clone https://github.com/equipa-gamma/ombela-market.git
cd ombela-market

# Instalar dependências do backend
cd backend
./mvnw clean install

# Instalar dependências do frontend
cd ../frontend
npm install

# Executar a aplicação
docker-compose up -d
testes
# Executar testes unitários
./mvnw test

# Executar testes de integração
./mvnw verify

# Ver cobertura de código
./mvnw jacoco:report
