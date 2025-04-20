
# Projeto: Análise de Mercado Cripto - Bitcoin Tracker

## 💡 Objetivo

Este projeto tem como objetivo inicial consultar o valor atual do Bitcoin utilizando uma arquitetura robusta e extensível: Arquitetura Hexagonal (Ports and Adapters).

A aplicação funcionará como uma API backend, que irá consumir a API da Binance para fornecer dados sobre criptomoedas. Essa API será futuramente consumida por uma interface web desenvolvida em React.

## 🎯 Funcionalidade Inicial

- Consultar o valor atual do Bitcoin a partir da API pública da Binance.

## 🏗️ Arquitetura Hexagonal

A aplicação está organizada com base na Arquitetura Hexagonal (Ports and Adapters), com as seguintes camadas/pacotes:

```
com.botcrypto.api
├── application       # Casos de uso (interage com o domínio)
├── domain            # Entidades, regras de negócio, interfaces (portas)
│   ├── model         # Entidades e objetos de valor
│   ├── service       # Regras de negócio puras
│   └── port
│       ├── in        # Interfaces que recebem chamadas (use cases)
│       └── out       # Interfaces que o domínio usa para se comunicar com o exterior
├── adapter
│   ├── in            # Entrada externa (REST controllers, CLI, eventos)
│   └── out           # Saída externa (Repositórios, APIs, bancos, etc.)
├── config            # Configurações do projeto (injeção de dependência, etc.)
```

## 🔮 Futuras Expansões

- Armazenar preços consultados para histórico e análise.
- Cadastrar compras de criptomoedas e comparar preços de aquisição.
- Visualização em dashboard com gráficos e tendências (via frontend React).
- Suporte a múltiplas moedas (Ethereum, Solana, etc.).

## 🛠️ Tecnologias previstas

- Linguagem: Java
- Framework: Spring Boot 
- API de cotação de mercado: [Binance](https://binance-docs.github.io/apidocs/)
- JSON parsing: Jackson
- (Futuramente) Banco de dados: MySql
- Frontend: React (em projeto separado)

---

## 🚀 Como Executar (em breve)

> Instruções para execução local serão adicionadas conforme o projeto evoluir.

---

## 📌 Observações

Este projeto está em estágio inicial e será desenvolvido passo a passo, com foco em clareza e aprendizado. O objetivo também é aplicar boas práticas de arquitetura desde o início.

---

## 📝 Padrão de Mensagens de Commits

Cada tipo de commit segue um padrão bem definido:

### 🚀 Funcionalidades novas
- **`feat:`** Para novas funcionalidades.
    - Exemplo: `feat(api): criar endpoint para consultar o preço do Bitcoin`

### 🐛 Correções de bugs
- **`fix:`** Para correções de bugs.
    - Exemplo: `fix(client): corrigir erro ao tratar resposta da Binance`

### 🔨 Refatorações de código
- **`refactor:`** Para refatorações de código sem alteração de comportamento.
    - Exemplo: `refactor(service): extrair lógica de cotação para classe separada`

### 📄 Alterações na documentação
- **`docs:`** Para alterações na documentação.
    - Exemplo: `docs: atualizar instruções de execução local`

### 🎨 Mudanças de estilo e formatação
- **`style:`** Para mudanças de estilo (formatação de código, etc.).
    - Exemplo: `style: remover espaços em branco desnecessários`

### 🧪 Testes
- **`test:`** Para adicionar ou modificar testes.
    - Exemplo: `test: adicionar teste unitário para cotaçãoService`

### 🧹 Tarefas diversas
- **`chore:`** Para tarefas diversas (build, configuração, etc.).
    - Exemplo: `chore: adicionar .gitignore para Maven e IntelliJ`