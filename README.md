# EcoBrain - Sistema de Controle Financeiro

## Visão Geral
O EcoBrain é um sistema completo de controle financeiro pessoal que permite aos usuários gerenciar suas finanças de forma eficiente e intuitiva. O sistema é composto por um backend em Ruby on Rails 8 e um frontend em React com TypeScript.

## Arquitetura

### Backend (Ruby on Rails 8)
- **API RESTful** com autenticação JWT
- **PostgreSQL** como banco de dados principal
- **RSpec** para testes
- **Rubocop** para linting
- **Sidekiq** para processamento assíncrono
- **Redis** para cache e filas

### Frontend (React + TypeScript)
- **Vite** como bundler
- **React Router** para navegação
- **Redux Toolkit** para gerenciamento de estado
- **Material-UI** para componentes de interface
- **Axios** para requisições HTTP
- **Jest** e **React Testing Library** para testes
- **ESLint** e **Prettier** para linting e formatação

## Funcionalidades Principais

### 1. Autenticação e Perfil
- Registro e login de usuários
- Recuperação de senha
- Perfil do usuário
- Configurações de conta
- Notificações por email

### 2. Dashboard Financeiro
- Visão geral das finanças
- Gráficos de receitas e despesas
- Saldo atual
- Previsão de gastos
- Metas financeiras

### 3. Transações
- Registro de receitas e despesas
- Categorização de transações
- Recorrência de transações
- Importação de extratos
- Anexos de comprovantes
- Tags personalizadas

### 4. Orçamento
- Planejamento mensal
- Categorias de orçamento
- Alertas de limite
- Acompanhamento de gastos por categoria
- Histórico de orçamentos

### 5. Relatórios
- Relatórios personalizados
- Exportação em PDF e Excel
- Análise de gastos
- Comparativos mensais/anuais
- Gráficos interativos

### 6. Metas Financeiras
- Definição de metas
- Acompanhamento de progresso
- Alertas de metas
- Sugestões de economia
- Histórico de conquistas

### 7. Investimentos
- Registro de investimentos
- Acompanhamento de carteira
- Rendimentos e perdas
- Diversificação de investimentos
- Alertas de mercado

## Modelos de Dados

### User
- email
- password_digest
- name
- avatar
- preferences
- settings

### Transaction
- amount
- description
- date
- type (income/expense)
- category_id
- user_id
- recurring
- attachment
- tags

### Category
- name
- type
- icon
- color
- user_id
- parent_id

### Budget
- amount
- month
- year
- category_id
- user_id
- spent_amount

### Goal
- title
- target_amount
- current_amount
- deadline
- user_id
- category_id
- status

### Investment
- name
- type
- amount
- purchase_date
- current_value
- user_id
- notes

## API Endpoints Principais

### Autenticação
- POST /api/v1/auth/register
- POST /api/v1/auth/login
- POST /api/v1/auth/refresh
- POST /api/v1/auth/forgot_password
- POST /api/v1/auth/reset_password

### Transações
- GET /api/v1/transactions
- POST /api/v1/transactions
- GET /api/v1/transactions/:id
- PUT /api/v1/transactions/:id
- DELETE /api/v1/transactions/:id
- GET /api/v1/transactions/summary

### Categorias
- GET /api/v1/categories
- POST /api/v1/categories
- PUT /api/v1/categories/:id
- DELETE /api/v1/categories/:id

### Orçamentos
- GET /api/v1/budgets
- POST /api/v1/budgets
- PUT /api/v1/budgets/:id
- GET /api/v1/budgets/summary

### Metas
- GET /api/v1/goals
- POST /api/v1/goals
- PUT /api/v1/goals/:id
- GET /api/v1/goals/progress

### Investimentos
- GET /api/v1/investments
- POST /api/v1/investments
- PUT /api/v1/investments/:id
- GET /api/v1/investments/portfolio

## Próximos Passos

### Fase 1: Configuração Inicial
1. Configurar ambiente de desenvolvimento
2. Implementar autenticação básica
3. Criar modelos principais
4. Configurar testes

### Fase 2: Funcionalidades Básicas
1. Implementar CRUD de transações
2. Criar sistema de categorias
3. Desenvolver dashboard básico
4. Implementar orçamento simples

### Fase 3: Funcionalidades Avançadas
1. Adicionar relatórios
2. Implementar metas
3. Desenvolver sistema de investimentos
4. Adicionar importação de dados

### Fase 4: Polimento e Otimização
1. Melhorar UI/UX
2. Otimizar performance
3. Adicionar testes automatizados
4. Implementar CI/CD

## Requisitos Técnicos

### Backend
- Ruby 3.2+
- Rails 8.0+
- PostgreSQL 14+
- Redis 6+

### Frontend
- Node.js 18+
- React 18+
- TypeScript 5+
- Vite 4+

## Segurança
- Autenticação JWT
- HTTPS obrigatório
- Rate limiting
- Sanitização de inputs
- Proteção contra CSRF
- Validação de dados
- Logs de segurança

## Performance
- Cache de consultas frequentes
- Paginação de resultados
- Otimização de queries
- Compressão de assets
- Lazy loading
- Code splitting

## Monitoramento
- Logs estruturados
- Métricas de performance
- Alertas de erro
- Monitoramento de uptime
- Analytics de uso

## Documentação
- API Documentation (OpenAPI/Swagger)
- Guia de contribuição
- Documentação de código
- Guia de estilo
- Tutorial de uso 