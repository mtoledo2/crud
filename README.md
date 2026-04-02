# Cadastro de Usuários — CRUD Fullstack

Aplicação fullstack de cadastro de usuários com operações de criação, leitura, atualização e exclusão (CRUD). O backend expõe uma API REST construída com Node.js + Express, utiliza o Prisma ORM para comunicação com o banco de dados MongoDB, e o frontend consome essa API para exibir e gerenciar os dados.

## Tecnologias

**Backend**
- Node.js com ES Modules
- Express 5
- Prisma 6 (ORM)
- MongoDB (banco de dados)
- CORS

**Frontend**
- HTML, CSS e JavaScript
- Axios (requisições HTTP)

## Estrutura do projeto

```
crud/
├── cadastro-usuarios/   # Frontend (HTML + CSS + JS)
├── prisma/              # Schema e migrations do banco
│   └── schema.prisma
├── server.js            # Servidor Express com as rotas da API
├── prisma.config.ts     # Configuração do Prisma
└── package.json
```

## Como rodar localmente

### Pré-requisitos

- Node.js 18+
- MongoDB rodando localmente ou URI de conexão (ex: MongoDB Atlas)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/mtoledo2/crud.git
cd crud

# Instale as dependências
npm install

# Crie o arquivo de variáveis de ambiente
cp .env.example .env
# Edite o .env com sua URI do MongoDB:
# DATABASE_URL="mongodb+srv://usuario:senha@cluster.mongodb.net/crud"
```

### Rodando

```bash
# Gera o Prisma Client
npx prisma generate

# Inicia o servidor backend
node server.js
```

Abra o arquivo `cadastro-usuarios/index.html` no navegador para acessar o frontend.

> **Observação:** O arquivo `.env` não está versionado por segurança. Você precisará configurar sua própria `DATABASE_URL` com a URI do MongoDB.

## Funcionalidades

- Cadastro de novos usuários
- Listagem de usuários cadastrados
- Edição de dados de um usuário
- Exclusão de usuários

## Próximas melhorias

- [ ] Deploy do backend (Render ou Railway)
- [ ] Deploy do frontend (Vercel)
- [ ] Validação de campos no frontend e no backend
- [ ] Autenticação com JWT
- [ ] Migrar frontend para React

## Autor

Murilo Toledo — [murilo-toledo.vercel.app](https://murilo-toledo.vercel.app)
