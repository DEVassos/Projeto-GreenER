# 🌱 GreenER — Plataforma de Monitoramento e Impacto Ambiental de Software

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Projeto de Aprendizagem Baseada em Projetos (ABP) — 2º Semestre DSM**  
**Faculdade de Tecnologia de Jacareí (FATEC Jacareí)**  
**Parceiro Acadêmico:** UniLaunch &middot; **Equipe:** DEVassos

</div>

---

## 📌 1. Visão Geral do Projeto

O **GreenER** é uma plataforma web de observabilidade socioambiental e **GreenOps** projetada para monitorar continuamente aplicações e microsserviços distribuídos em nuvem. 

A ferramenta traduz métricas computacionais brutas de infraestrutura (**CPU, Memória RAM, Disco e Rede**) em indicadores claros e acionáveis de **consumo energético (kWh)** e **pegada de carbono estimada em gramas de CO₂ equivalente (gCO₂e)**, correlacionando o consumo de hardware com a intensidade de carbono da matriz energética regional onde o serviço está hospedado.

> 💡 **Princípio Central:** Software não consome energia diretamente, mas o hardware que o executa sim. O GreenER atua como uma ponte analítica entre infraestrutura de TI e metas corporativas de sustentabilidade e ESG.

---

## 👥 2. Integrantes da Equipe (**DEVassos**)

| Avatar | Integrante | Função / Papel | GitHub |
| :---: | :--- | :--- | :---: |
| <img src="https://github.com/travensolli.png" width="60" style="border-radius:50%;" alt="Gabriel Travensolli" /> | **Gabriel Travensolli** | Scrum Master / Desenvolvedor Front-end | [@travensolli](https://github.com/travensolli) |
| <img src="https://github.com/henriqueptbd-cell.png" width="60" style="border-radius:50%;" alt="Henrique Camargo" /> | **Henrique Camargo** | Product Owner (PO) | [@henriqueptbd-cell](https://github.com/henriqueptbd-cell) |
| <img src="https://github.com/DeaTuribio.png" width="60" style="border-radius:50%;" alt="Andrea Turibio" /> | **Andrea Turibio** | Desenvolvedora Front-end | [@DeaTuribio](https://github.com/DeaTuribio) |
| <img src="https://github.com/LUCASAMR23.png" width="60" style="border-radius:50%;" alt="Lucas Amorim" /> | **Lucas Amorim** | Desenvolvedor Back-end | [@LUCASAMR23](https://github.com/LUCASAMR23) |
| <img src="https://github.com/viniciusaugusto1997.png" width="60" style="border-radius:50%;" alt="Vinicius Augusto" /> | **Vinicius Augusto** | Desenvolvedor Back-end | [@viniciusaugusto1997](https://github.com/viniciusaugusto1997) |

---

## 🎯 3. Principais Funcionalidades e Diferenciais

- **Descoberta Dinâmica de Serviços:** Ingestão periódica resiliente via API (`/services` e `/metrics`), identificando adições, remoções e quedas de microsserviços sem intervenção manual e sem travar a coleta.
- **Motor de Cálculo Socioambiental:** Aplicação rigorosa das equações de Green Software para conversão de recursos em Potência (W), Energia (kWh) e emissões de carbono (gCO₂e) ponderadas pelo fator regional da API de intensidade de carbono.
- **Dashboard em Três Níveis de Experiência:**
  - **Nível 1 (Visão Executiva):** Indicadores agregados em tempo real (kWh total, gCO₂e acumulado, status dos serviços ativos/indisponíveis) com atualização sem reload.
  - **Nível 2 (Distribuição e Análise Comparativa):** Ranking dos principais emissores e distribuição geográfica de emissões.
  - **Nível 3 (Investigação Detalhada):** Histórico temporal de telemetria por serviço, curvas de carga e variação de potência.
- **Simulação de Migração Regional:** Estimativa de economia de carbono ao simular a transferência de serviços para regiões com matriz energética mais limpa.
- **Mecanismo Global de Exportação:** Relatórios executivos em **PDF estilizado** e exportação de dados brutos em **CSV** para auditoria e relatórios corporativos de ESG.
- **Área Restrita Autenticada:** Controle de acesso administrativo seguro com tokens **JWT** e senhas criptografadas via **bcrypt**.

---

## 🛠️ 4. Stack Tecnológica e Restrições Arquiteturais

O projeto foi construído atendendo rigorosamente aos padrões de qualidade e restrições do edital (RP01 a RP07):

- **Front-end:** [React](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/) + [Vite](https://vitejs.dev/) + [Tailwind CSS](https://tailwindcss.com/)
- **Back-end:** [Node.js](https://nodejs.org/) + [TypeScript](https://www.typescriptlang.org/) estruturado em arquitetura modular (Controllers, Services, Repositories)
- **Banco de Dados:** [PostgreSQL](https://www.postgresql.org/) nativo utilizando **SQL puro parametrizado** via driver `pg` (**100% livre de ORM**)
- **Segurança & Autenticação:** [JWT (JSON Web Tokens)](https://jwt.io/) e [bcrypt](https://github.com/kelektiv/node.bcrypt.js)
- **Infraestrutura & Deploy:** [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) com volume persistente para banco de dados

---

## 🗓️ 5. Cronograma e Entregas das Sprints

| Sprint | Período / Review | Foco Principal | Entregáveis Chave |
| :---: | :---: | :--- | :--- |
| **Sprint 1** | 19/10/2026 | **MVP Operacional, Ingestão, Auth & Docker** | Ingestão resiliente, motor de cálculo, persistência SQL puro, Dashboard Nível 1 com KPIs em tempo real, exportação PDF/CSV, Auth JWT e ambiente Docker completo. |
| **Sprint 2** | 09/11/2026 | **Análises Avançadas, Histórico & Visualização** | Consultas temporais agregadas, gráficos de tendências históricas, ranking de eficiência e visualização espacial em mapa de calor/bolhas. |
| **Sprint 3** | 23/11/2026 | **Comparações, Simulação de Migração & Polimento** | Módulo comparativo lado a lado, simulador de migração para regiões limpas, refinamento de relatórios e validação final de carga. |

---

## 🚀 6. Como Executar a Aplicação Localmente

### Pré-requisitos
- [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/) instalados na máquina.
- [Git](https://git-scm.com/) para clonar o repositório.

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/DEVassos/Projeto-GreenER.git
   cd Projeto-GreenER
   ```

2. **Configure as variáveis de ambiente:**
   ```bash
   cp .env.example .env
   ```

3. **Suba todo o ecossistema com um único comando:**
   ```bash
   docker compose up --build
   ```

4. **Acesse no navegador:**
   - **Frontend:** `http://localhost:5173` (ou porta configurada)
   - **Backend API:** `http://localhost:3000`
   - **Healthcheck:** `http://localhost:3000/health`

---

## 📂 7. Documentação Completa do Projeto

Para conferir detalhes aprofundados sobre regras de negócio, modelagem, endpoints e atas, consulte os documentos complementares:

- 📄 [Visão do Produto (`visao-do-produto.md`)](visao-do-produto.md) — Personas, fronteira de escopo e metas de produto.
- 📐 [Raciocínio Técnico & Arquitetura (`abp-2026-2.md`)](abp-2026-2.md) — Algoritmo de reconciliação e integrações.
- 📋 [Product Backlog Geral (`product-backlog.md`)](product-backlog.md) — Épicos, User Stories e critérios de aceitação.
- ⏱️ [Planejamento da Sprint 1 (`sprints/sprint-1.md`)](sprints/sprint-1.md) — Detalhamento de tarefas, pontuações e DoD da Sprint 1.
- 🔌 [Especificação de APIs (`especificacao-api.md`)](especificacao-api.md) — Contratos e endpoints das APIs externas.

---

<div align="center">
Desenvolvido com 💚 pela equipe <strong>DEVassos</strong> &middot; FATEC Jacareí 2026
</div>
