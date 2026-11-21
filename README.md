# 🧪 Plano de Testes QA Manual — Aplicativo iFood (iOS)

> **Projeto de Garantia de Qualidade (QA)** focado no mapeamento de funcionalidades, elaboração de casos de teste, execução funcional, reporte de bugs reais e emissão de parecer técnico de release.

---

## 📌 Sobre o Projeto

Este projeto avalia a versão comercial do aplicativo **iFood no iOS (v10.146.0)**.

O objetivo foi validar a estabilidade das principais jornadas do usuário, aplicando técnicas formais de teste manual, registrando métricas de execução e reportando falhas técnicas com evidências visuais.

---

## 🛠️ Informações do Ambiente e Escopo

- **Aplicativo:** iFood
- **Plataforma:** iOS
- **Versão:** 10.146.0
- **Escopo Testado:** Busca e filtragem, visualização de cardápios e detalhes, gerenciamento da sacola, substituição de estabelecimento, histórico de pedidos e Central de Notificações.

---

## 🗺️ Mapa de Funcionalidades e Priorização

| ID | Funcionalidade | Prioridade | Justificativa |
|:---|:---|:---:|:---|
| **F01** | Busca de restaurantes, produtos e filtros | **Alta** | Localização de estabelecimentos; falhas bloqueiam o início da jornada. |
| **F02** | Visualização de cardápio e produtos | **Alta** | Apresentação de itens e preços; essencial para a escolha. |
| **F03** | Adição e gerenciamento da sacola | **Alta** | Montagem do pedido; falhas impedem a conversão final de vendas. |
| **F04** | Troca de estabelecimento na sacola | **Média** | Regra de negócio de sacola única por loja. |
| **F05** | Consulta de histórico de pedidos | **Baixa** | Acompanhamento e checagem de compras anteriores. |
| **F06** | Central de Notificações | **Média** | Recebimento de comunicados, avisos e cupons promocionais. |

---

## 📊 Métricas de Execução dos Testes

Ao todo, foram elaborados e executados **17 Casos de Teste (CT-01 a CT-17)**, cobrindo caminhos positivos e cenários negativos.

| Resultado | Quantidade | Percentual |
|:---|:---:|:---:|
| 🟢 Aprovados (Passou) | 15 | 88,20% |
| 🔴 Reprovados (Falhou) | 2 | 11,80% |
| ⚪ Bloqueados | 0 | 0,00% |
| **Total Executado** | **17** | **100%** |

---

## 🐞 Bugs Reais Mapeados e Reportados

### 1. BUG-01 — Lentidão na Central de Notificações

- **Severidade:** Média
- **Frequência:** Às vezes
- **CT Vinculado:** CT-17
- **Ambiente:** iFood v10.146.0 | iOS | Wi-Fi/4G
- **Comportamento:** Ao acessar a aba de Notificações com conexão ativa, o aplicativo apresenta tela de carregamento contínuo por **28 segundos** até renderizar a lista.
- **Evidência:** `BUG-01_CT-17_LentidaoAbaNotificacoes_21-11-2026.mp4`

### 2. BUG-02 — Perda dos Filtros na Navegação

- **Severidade:** Média
- **Frequência:** Às vezes
- **CT Vinculado:** CT-04
- **Ambiente:** iFood v10.146.0 | iOS | Wi-Fi/4G
- **Comportamento:** Ao buscar por "açaí" e aplicar os filtros "Entrega Grátis" + "Avaliação", os filtros são resetados ao clicar em "Ver todos os restaurantes", exibindo lojas com taxa de entrega cobrada.
- **Evidência:** `BUG-02_CT-04_PerdaFiltrosEntregaGratisAvaliacao_21-11-2026.mp4`

---

## 🎯 Parecer Técnico e Recomendação Final

**Recomendação: Pode lançar com ressalvas.**

**Justificativa:**

Os fluxos críticos do negócio (busca básica, navegabilidade em cardápios, adição e alteração na sacola, regra de loja única e histórico de pedidos) apresentaram **100% de aprovação**.

Os dois bugs identificados (BUG-01 e BUG-02) afetam a usabilidade e o desempenho da aplicação, mas não impedem diretamente a conclusão de compras.

Recomenda-se o lançamento comercial com correção planejada para o próximo ciclo de manutenção (*patch release*).

---

**Projeto desenvolvido para prática de QA Manual**, contemplando planejamento, priorização de funcionalidades, elaboração e execução de casos de teste, documentação de evidências, identificação de defeitos e parecer técnico.

---

## 🤝 Créditos e Agradecimentos

Projeto desenvolvido com base na metodologia, diretrizes e Kit de QA da comunidade **Bora na Tech**.
