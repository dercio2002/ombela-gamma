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
### 3.2 Ferramentas Recomendadas

| Tipo | Ferramenta | Formato |
|------|------------|---------|
| UML | PlantUML | `.plantuml` (texto) |
| UML | draw.io / diagrams.net | `.drawio` |
| Base de Dados | MySQL Workbench | `.mwb` |
| Arquitetura | draw.io | `.drawio` |

### 3.3 Exemplos de Arquivos PlantUML

**Diagrama de Classes (exemplo simplificado):**

```plantuml
@startuml Diagrama_Classes
skinparam classAttributeIconSize 0

package "Domain" {
    abstract class Entidade {
        # id: Long
        # dataCriacao: LocalDateTime
        # dataAtualizacao: LocalDateTime
    }
    
    class Utilizador extends Entidade {
        - nome: String
        - email: String
        - senha: String
        - telefone: String
        - tipo: TipoUtilizador
        + validar()
        + autenticar(senha: String): boolean
    }
    
    class Produto extends Entidoid {
        - nome: String
        - descricao: String
        - preco: BigDecimal
        - stock: Integer
        - categoria: Categoria
        - imagens: List<String>
        + atualizarStock(quantidade: int)
    }
    
    class Pedido extends Entidade {
        - numero: String
        - status: StatusPedido
        - itens: List<ItemPedido>
        - total: BigDecimal
        - cliente: Utilizador
        + calcularTotal()
        + atualizarStatus(status: StatusPedido)
    }
    
    class ItemPedido {
        - quantidade: Integer
        - precoUnitario: BigDecimal
    }
}

package "Application" {
    interface IUtilizadorRepository {
        + findByEmail(email: String): Utilizador
        + save(utilizador: Utilizador): Utilizador
    }
    
    interface IProdutoRepository {
        + findByCategoria(categoria: Categoria): List<Produto>
        + findAll(): List<Produto>
    }
    
    class UtilizadorService {
        - repository: IUtilizadorRepository
        + cadastrar(dto: UtilizadorDTO): Utilizador
        + autenticar(credentials: LoginDTO): TokenDTO
    }
}

Utilizador "1" --> "*" Pedido : realiza
Pedido "1" --> "*" ItemPedido : contém
ItemPedido "*" --> "1" Produto : refere
UtilizadorService --> IUtilizadorRepository : usa
@enduml

# Commit inicial do projeto
git commit -m "chore: initialize project structure with Spring Boot"

# Nova funcionalidade
git commit -m "feat(auth): implement JWT authentication

- Add JWT token generation
- Create authentication filter
- Implement login endpoint
- Add password encryption with BCrypt"

# Correção de bug
git commit -m "fix(cart): resolve null pointer when removing last item

The cart service was throwing NPE when removing the last item from
the cart because the list was being cleared without null check.

Closes #42"

# Documentação
git commit -m "docs: update README with installation instructions"

# Refatoração
git commit -m "refactor(payment): extract payment processors to strategy pattern

- Create IProcessadorPagamento interface
- Implement PagamentoTransferencia and PagamentoReferencia
- Remove conditional logic from PagamentoService"

# Atualização do diagrama
git commit -m "docs(diagram): update class diagram with new attributes

Added 'telefone' and 'tipo' attributes to Utilizador class
Updated relationships to reflect new domain model"
a1b2c3d (HEAD -> main) feat(checkout): implement payment processing flow
e5f6g7h refactor(order): extract OrderService into smaller services
i9j0k1l fix(product): resolve image upload path issue
m2n3o4p docs: update API documentation
q5r6s7t feat(cart): add shopping cart persistence
u8v9w0x style: format code according to lint rules
y1z2a3b test(cart): add unit tests for CartService
c4d5e6f refactor(auth): apply DIP for UserRepository
f7g8h9i docs: add class diagram to architecture section
j0k1l2m feat(auth): implement user registration endpoint
n3o4p5q chore: setup initial project structure

main                    # Branch principal (produção)
develop                 # Branch de desenvolvimento
feature/[功能描述]       # Novas funcionalidades
bugfix/[descrição]      # Correções de bugs
hotfix/[descrição]      # Correções urgentes em produção
release/[versão]        # Preparação de releases
## Code Review Checklist

### Funcionalidade
- [ ] A funcionalidade funciona conforme especificado?
- [ ] Todos os critérios de aceitação foram atendidos?

### Código
- [ ] O código segue os princípios SOLID?
- [ ] Os nomes são descritivos e significativos?
- [ ] O código está DRY (Don't Repeat Yourself)?
- [ ] Os métodos são pequenos e com uma responsabilidade?

### Testes
- [ ] Existem testes unitários para a nova funcionalidade?
- [ ] Os testes cobrem os casos de borda?
- [ ] Os testes passam?

### Segurança
- [ ] Validação de entrada implementada?
- [ ] Não há exposição de dados sensíveis?
- [ ] Queries parametrizadas prevenem SQL Injection?

### Observações
> Adicione comentários construtivos aqui

**Status:** ✅ Aprovado / 🔄 Solicitar Alterações / ❌ Rejeitado

# Ombela Market - Product Backlog

## User Stories por Prioridade

### Must Have (MVP)

| ID | User Story | Pontos | Sprint |
|----|------------|--------|--------|
| US01 | Como cliente, quero me cadastrar no sistema para criar uma conta | 3 | Sprint 1 |
| US02 | Como cliente, quero fazer login para acessar minha conta | 2 | Sprint 1 |
| US03 | Como vendedor, quero cadastrar produtos com fotos para vendê-los | 5 | Sprint 1 |
| US04 | Como cliente, quero visualizar o catálogo de produtos | 3 | Sprint 1 |
| US05 | Como cliente, quero pesquisar produtos por nome/categoria | 3 | Sprint 2 |
| US06 | Como cliente, quero adicionar produtos ao carrinho | 5 | Sprint 2 |
| US07 | Como cliente, quero finalizar compra com pagamento | 8 | Sprint 2 |
| US08 | Como cliente, quero acompanhar status do meu pedido | 5 | Sprint 3 |

### Should Have

| ID | User Story | Pontos | Sprint |
|----|------------|--------|--------|
| US09 | Como cliente, quero receber notificações por email | 5 | Sprint 3 |
| US10 | Como vendedor, quero gerenciar meu inventário | 5 | Sprint 3 |
| US11 | Como cliente, quero avaliar produtos comprados | 8 | Sprint 4 |
| US12 | Como administrador, quero gerar relatórios de vendas | 8 | Sprint 4 |

### Could Have

| ID | User Story | Pontos |
|----|------------|--------|
| US13 | Como cliente, quero compartilhar produtos nas redes sociais | 5 |
| US14 | Como vendedor, quero definir promoções e descontos | 8 |
| US15 | Como cliente, quero salvar produtos em lista de desejos | 3 |

### Won't Have (MVP)

| ID | User Story | Razão |
|----|------------|-------|
| US16 | Chat em tempo real | Fora do escopo MVP |
| US17 | Sistema de fidelização | Fase 2 do projeto |
| US18 | Integração com transportadoras | Requer parcerias externas |

---

## Definition of Ready

Uma user story está "READY" para ser implementada quando:
- [ ] Tem uma descrição clara (formato: Como [ator], quero [ação], para [benefício])
- [ ] Critérios de aceitação estão definidos (Given-When-Then)
- [ ] Estimativa de pontos de história foi atribuída
- [ ] Dependências estão identificadas
- [ ] O Product Owner validou a story

---

## Sprints Realizadas

### Sprint 0: Foundation
**Período:** [data] a [data]
**Objetivo:** Setup do projeto, configuração de ambiente

### Sprint 1: Core Authentication & Products
**Período:** [data] a [data]
**Objetivo:** Autenticação e gestão de produtos

### Sprint 2: Catalog & Cart
**Período:** [data] a [data]
**Objetivo:** Catálogo, pesquisa e carrinho de compras

### Sprint 3: Checkout & Notifications
**Período:** [data] a [data]
**Objetivo:** Finalização de compras e notificações

---

## Métricas do Projeto

| Métrica | Valor |
|---------|-------|
| Total de User Stories | 18 |
| Pontos Totais | 85 |
| Velocity Médio | 21 pontos/sprint |
| Sprints Realizadas | 4 |

com.ombela.market
├── presentation      # Controllers, DTOs, ViewModels
├── application       # Use Cases, Services
├── domain            # Entidades, Exceções do domínio
├── infrastructure    # Persistência, APIs externas
└── security          # Auth, JWT, Filters

# 1. Atualizar a branch develop
git checkout develop
git pull origin develop

# 2. Criar branch para a funcionalidade
git checkout -b feature/minha-funcionalidade

# 3. Desenvolver e commitar frequentemente
git add .
git commit -m "feat(module): description of changes"

# 4. Sincronizar com develop (rebase)
git fetch origin
git rebase origin/develop

# 5. Resolver conflitos se necessário

# 6. Fazer push
git push -u origin feature/minha-funcionalidade

# 7. Criar Pull Request
# Aceder ao GitHub e criar PR para develop

# 8. Após aprovação, fazer merge
# Criar tag para release
git tag -a v1.0.0 -m "Release version 1.0.0"

# push tag
git push origin v1.0.0

# Formato de versão: MAJOR.MINOR.PATCH
# MAJOR: Breaking changes
# MINOR: New features (backwards compatible)
# PATCH: Bug fixes


