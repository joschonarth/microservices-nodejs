<div align="center">

# 🧩 Microsserviços Escaláveis com Node

_Sistema distribuído com microsserviços, mensageria, observabilidade e infraestrutura como código._

---

📃 [Sobre](#-sobre)&nbsp;&nbsp;•&nbsp;&nbsp;
🛠️ [Tecnologias](#️-tecnologias)&nbsp;&nbsp;•&nbsp;&nbsp;
🧠 [Conceitos Aplicados](#-conceitos-aplicados)&nbsp;&nbsp;•&nbsp;&nbsp;
🏗️ [Arquitetura](#️-arquitetura)

</div>

---

## 📃 Sobre

Este projeto é um sistema distribuído construído do zero, composto por dois microsserviços — **pedidos** e **faturas** — que se comunicam de forma assíncrona via mensageria, expostos através de um API Gateway e implantados na AWS usando infraestrutura como código. O foco está na aplicação prática de conceitos fundamentais de arquitetura de microsserviços, observabilidade e infraestrutura como código, explorando desafios reais de sistemas distribuídos como latência, consistência de dados e idempotência.

---

## 🛠️ Tecnologias

- 🟩 **[Node.js](https://nodejs.org/)** — Ambiente de execução JavaScript utilizado em ambos os microsserviços.
- 🟦 **[TypeScript](https://www.typescriptlang.org/)** — Tipagem estática e segurança em tempo de desenvolvimento.
- 🔥 **[Fastify](https://fastify.dev/)** — Framework web utilizado na construção das APIs dos serviços.
- 🐇 **[RabbitMQ](https://www.rabbitmq.com/)** — Message broker para comunicação assíncrona entre os serviços.
- 🐘 **[PostgreSQL](https://www.postgresql.org/)** — Banco de dados relacional utilizado pelos serviços.
- 🐳 **[Docker](https://www.docker.com/)** — Containerização dos serviços e dependências para desenvolvimento local.
- 🗃️ **[Drizzle ORM](https://orm.drizzle.team/)** — ORM leve e type-safe para acesso ao banco de dados.
- 🦍 **[Kong](https://konghq.com/products/kong-gateway)** — API Gateway responsável pelo roteamento, autenticação e gerenciamento de tráfego.
- ☁️ **[AWS](https://aws.amazon.com/)** — Provedor de nuvem utilizado para o deploy da aplicação.
- 🏗️ **[Pulumi](https://www.pulumi.com/)** — Infraestrutura como código para provisionamento e gerenciamento dos recursos na AWS.
- 🔭 **[OpenTelemetry](https://opentelemetry.io/)** — Instrumentação para coleta de traces distribuídos.
- 🕵️ **[Jaeger](https://www.jaegertracing.io/)** — Visualização e análise de distributed tracing entre os serviços.
- 📊 **[Grafana](https://grafana.com/)** — Monitoramento e visualização de métricas dos serviços.

---

## 🧠 Conceitos Aplicados

- 🔍 **Distributed Tracing** — Requisições são rastreadas de ponta a ponta entre os serviços, permitindo diagnosticar gargalos e falhas em um fluxo distribuído.
- 🧩 **Separação por domínio** — Os serviços são divididos por domínio de negócio (pedidos e faturas), e não por camadas técnicas.
- ⚡ **Latência e consistência de dados** — A comunicação entre serviços é projetada considerando os trade-offs entre performance e consistência dos dados.
- 🔁 **Idempotência** — As operações críticas são implementadas de forma a suportar reprocessamento sem gerar efeitos colaterais indesejados.
- 🐇 **Mensageria assíncrona** — Os serviços se comunicam de forma desacoplada através do RabbitMQ, sem dependência direta entre si.
- 🏗️ **Infraestrutura como código (IaC)** — Toda a infraestrutura na AWS é provisionada e versionada via Pulumi.
- 🚪 **API Gateway** — O Kong atua como ponto único de entrada, roteando requisições, centralizando autenticação e gerenciando o tráfego entre os serviços.
- 🔀 **Proxy** — Utilizado como camada de encaminhamento de requisições entre cliente e servidor, sem as responsabilidades adicionais de um Gateway.
- ⚖️ **Load Balancer** — Distribui a carga entre as instâncias dos serviços para garantir escalabilidade.
- 🔐 **Autenticação em microsserviços** — A autenticação é centralizada no Gateway, evitando duplicidade de lógica em cada serviço.
- 👀 **Observabilidade** — Tracing, métricas e logs são combinados para acompanhar o comportamento do sistema em tempo real.
- 🔄 **DevOps e CI/CD** — Pipelines e variáveis de ambiente são utilizados para automatizar o build, teste e deploy dos serviços.

---

## 🏗️ Arquitetura

O sistema é composto por:

- **Serviço de Pedidos** — Responsável pela criação e gerenciamento de pedidos.
- **Serviço de Faturas** — Responsável pela geração de faturas a partir dos pedidos.
- **RabbitMQ** — Broker de mensageria que conecta os dois serviços de forma assíncrona e desacoplada.
- **Kong (API Gateway)** — Ponto único de entrada, responsável por rotear as requisições, autenticar e gerenciar o tráfego entre os serviços.
- **PostgreSQL** — Banco de dados de cada serviço.
- **Jaeger + OpenTelemetry** — Camada de observabilidade para distributed tracing entre os serviços.
- **Grafana** — Monitoramento e visualização de métricas da aplicação.
- **AWS + Pulumi** — Infraestrutura provisionada como código para o deploy dos serviços na nuvem.

---

<div align="center">

Feito com ♥ por **[João Otávio Schonarth](https://github.com/joschonarth)**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/joschonarth)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/joschonarth)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joschonarth@gmail.com)

</div>
