<div align="center">

# 🚀 Olist Data Labs

### **Ecossistema de Engenharia de Dados, IA & DevOps**
*Projeto Integrado — Faculdade UNIFEOB (2026)*

[![ADS](https://img.shields.io/badge/Curso-ADS-blue?style=for-the-badge&logo=codecademy&logoColor=white)](#)
[![Ciência da Computação](https://img.shields.io/badge/Curso-Ci%C3%AAncia%20da%20Computa%C3%A7%C3%A3o-darkgreen?style=for-the-badge&logo=computer&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-orange?style=for-the-badge)](#)

---

<p align="center">
  Uma plataforma completa de <b>Inteligência Logística e Análise Preditiva para E-commerce</b>,<br>
  construída sobre o dataset real da <b>Olist Marketplace</b>.
</p>

</div>

---

## 📌 Sobre o Projeto & Contexto Empresarial

O **Olist Data Labs** foi concebido para simular uma arquitetura corporativa moderna de solução de Big Data e Inteligência Artificial baseada em uma operação real de e-commerce.

### 🏢 A Empresa Real: Olist
A **Olist** é uma *unicorn startup* brasileira que atua como um ecossistema de soluções para e-commerce. O seu principal produto funciona como um **integrador de marketplace**: ela conecta pequenos e médios lojistas (*sellers*) aos maiores canais de venda do país (Mercado Livre, Amazon, Magalu, Casas Bahia, etc.), centralizando a gestão de estoque, pedidos e toda a operação de **logística e envio**.

### 📊 O Dataset Público da Olist
Utilizamos o dataset público da Olist contendo mais de **100.000 pedidos reais** realizados no e-commerce brasileiro entre 2016 e 2018. A base de dados engloba múltiplos pontos de contato da jornada do consumidor:
* **Logística:** Status de pedidos, datas estimadas vs. datas reais de entrega, peso e localização (CEPs).
* **Financeiro:** Valores de frete, preço de produtos e meios de pagamento.
* **Experiência do Cliente:** Avaliações, notas (*review scores*) e comentários dos compradores.

### 🎯 Nosso Objetivo Tecnológico
A partir desse volume de dados real, a nossa plataforma realiza a **ingestão, modelagem e tratamento (ETL)**, processa métricas para **Análise Exploratória (AED)** e disponibiliza um **modelo preditivo de Machine Learning** capaz de prever em tempo real o **risco de atraso logístico e a probabilidade de insatisfação do cliente**.

---

## 🏗️ Arquitetura do Sistema (Microserviços)

O ecossistema é dividido de forma **desacoplada e modular em 3 camadas**:

```text
 ┌─────────────────────────────────────────────────────────────────────────┐
 │                        🎨 olist-frontend (Next.js)                      │
 └────────────────────────────────────┬────────────────────────────────────┘
                                      │
                                      │ 1. Requisições REST / JSON
                                      ▼
 ┌─────────────────────────────────────────────────────────────────────────┐
 │                        ⚡ olist-backend (Node.js/TS)                     │
 └──────────────┬──────────────────────────────────────────┬───────────────┘
                │                                          │
                │ 2. Salva / Consulta                      │ 3. Executa Predição
                ▼                                          ▼
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │ 🐘 PostgreSQL (Docker)       │          │ 🧠 olist-ai-service (Python) │
 └──────────────────────────────┘          └──────────────────────────────┘
