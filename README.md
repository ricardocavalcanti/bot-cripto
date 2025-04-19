
# Projeto: Análise de Mercado Cripto - Bitcoin Tracker

## 💡 Objetivo

Este projeto tem como objetivo inicial consultar o valor atual do **Bitcoin** utilizando uma arquitetura robusta e extensível: **Arquitetura Hexagonal (Ports and Adapters)**.

A ideia é criar um sistema modular e bem estruturado, que possa futuramente evoluir para análises mais completas do mercado cripto e integração com dados de compras pessoais.

## 🎯 Funcionalidade Inicial

- Consultar o valor atual do **Bitcoin** a partir de uma API externa.

## 🏗️ Arquitetura Hexagonal

A aplicação está organizada com base na Arquitetura Hexagonal (Ports and Adapters), com as seguintes camadas/pacotes:

```
com.seuprojeto
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
- Visualização em dashboard com gráficos e tendências.
- Suporte a múltiplas moedas (Ethereum, Solana, etc.).

## 🛠️ Tecnologias previstas

- Linguagem: Java
- Framework: Spring Boot 
- API de cotação de mercado: Binance
- JSON parsing: Jackson
- (Futuramente) Banco de dados: MySql

---

## 🚀 Como Executar (em breve)

> Instruções para execução local serão adicionadas conforme o projeto evoluir.

---

## 📌 Observações

Este projeto está em estágio inicial e será desenvolvido passo a passo, com foco em clareza e aprendizado. O objetivo também é aplicar boas práticas de arquitetura desde o início.
