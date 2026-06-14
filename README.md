<h1 align="center">⚽ Brasileirão · Busca por Formação Tática</h1>

<p align="center">
  Encontre partidas do <b>Brasileirão Série A</b> filtrando pela formação tática dos times — com análise gerada por <b>IA local</b>.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-20.x-339933?style=flat-square&logo=node.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-IA%20local-000000?style=flat-square&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/>
</p>

---

## 🎯 Sobre

Aplicação web que permite **pesquisar partidas do Brasileirão por formação tática** (ex.: `4-3-3`, `4-4-2`) e obter uma **análise automática** do confronto gerada por um modelo de linguagem rodando **localmente via Ollama** — sem depender de APIs pagas.

## ✨ Funcionalidades

- 🔍 Busca de partidas por formação tática dos times.
- 🤖 Análise tática das partidas gerada por **IA local (Ollama)**.
- 🗄️ Dados persistidos em **PostgreSQL**.
- 🌐 Interface web servida pelo próprio backend Express.

## 🛠️ Stack

| Camada | Tecnologia |
|---|---|
| Backend | Node.js 20 · Express |
| Banco | PostgreSQL (`pg`) |
| IA | Ollama (modelo local) |
| HTTP | Axios |
| Front | HTML/CSS/JS (`public/`) |

## 🚀 Como rodar

> Pré-requisitos: **Node 20+**, **PostgreSQL** e **[Ollama](https://ollama.com)** instalado e rodando.

```bash
# 1. Instalar dependências
npm install

# 2. Configurar variáveis de ambiente (.env)
#    DATABASE_URL=postgres://usuario:senha@host:5432/banco
#    (e demais variáveis usadas no projeto)

# 3. Criar e popular o banco
node generate-sql.js   # gera o SQL de criação
node seed.js           # popula com os dados das partidas

# 4. Garantir o modelo no Ollama (ex.: llama3.2)
ollama pull llama3.2

# 5. Subir o servidor
npm start              # http://localhost:3000
```

## 📁 Estrutura

```
server.js          — servidor Express e rotas
db.js              — conexão com o PostgreSQL
ai.js              — integração com o Ollama (análise por IA)
api/analysis.js    — endpoint de análise
generate-sql.js    — geração do schema SQL
seed.js            — carga inicial de dados
migrations/        — migrations do banco
public/index.html  — interface web
```

---

<p align="center">
  Projeto pessoal de <b>Antonio Carvalho</b> · futebol + dados + IA local 🧠⚽
</p>
