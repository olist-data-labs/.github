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

## 📌 Sobre o Projeto

O **Olist Data Labs** foi concebido para simular uma arquitetura corporativa moderna de solução de Big Data e Inteligência Artificial. 

A plataforma realiza a ingestão e tratamento de dados brutos de logística de e-commerce, processa estatísticas avançadas e fornece um **modelo preditivo de Machine Learning** capaz de prever **riscos e probabilidades de atraso nas entregas** em tempo real.

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
 │                        ⚡ olist-backend (Node.js/TS)                    │
 └──────────────┬──────────────────────────────────────────┬───────────────┘
                │                                          │
                │ 2. Salva / Consulta                      │ 3. Executa Predição
                ▼                                          ▼
 ┌──────────────────────────────┐          ┌──────────────────────────────┐
 │ 🐘 PostgreSQL (Docker)      │          │ 🧠 olist-ai-service (Python) │
 └──────────────────────────────┘          └──────────────────────────────┘
