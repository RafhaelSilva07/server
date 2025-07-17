# NLW Agents

Projeto desenvolvido durante o evento **NLW da Rocketseat**, com foco na construção de uma API moderna, eficiente e escalável.

 Tecnologias Utilizadas

- **Node.js** com **TypeScript**
- **Fastify** – Framework web rápido
- **PostgreSQL** com extensão `pgvector`
- **Drizzle ORM** – Operações type-safe com banco de dados
- **Zod** – Validação de schemas
- **Docker** e **Docker Compose** – Ambiente isolado
- **Biome** – Lint e formatação de código

Arquitetura

- Estrutura modular por responsabilidade (rotas, schemas, banco)
- Validação robusta com Zod
- ORM moderno com Drizzle
- Configuração centralizada via `.env`

Como Rodar o Projeto

Pré-requisitos

- Node.js (com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

Passos

```bash
# 1. Clone o repositório
git clone <url-do-repositorio>
cd server

# 2. Suba o banco de dados
docker-compose up -d

# 3. Configure as variáveis de ambiente
cp .env.example .env
# Edite o arquivo .env conforme necessário

# 4. Instale as dependências
npm install

# 5. Rode as migrações
npx drizzle-kit migrate

# 6. (Opcional) Popule o banco com dados de exemplo
npm run db:seed

# 7. Inicie o servidor
npm run dev  # desenvolvimento
# ou
npm start    # produção
