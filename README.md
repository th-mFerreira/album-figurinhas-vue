# ⚽ Álbum de Figurinhas das Seleções

Projeto desenvolvido em Vue 3 utilizando a API-Football para exibir o elenco de jogadores das seleções nacionais em formato de álbum de figurinhas.

## 📋 Descrição

A aplicação permite selecionar um país através de uma lista dinâmica carregada pela API-Football. Após a seleção, o sistema realiza consultas encadeadas para identificar a seleção correspondente e exibir seu elenco de jogadores.

Cada jogador é apresentado em um card contendo:

- Foto oficial
- Nome
- Posição traduzida para português

Além disso, a aplicação exibe:

- Nome do país traduzido para português
- Bandeira da seleção escolhida
- Quantidade total de jogadores carregados

---

## 🚀 Tecnologias Utilizadas

- Vue 3
- Vite
- JavaScript
- HTML5
- CSS3
- API-Football
- Git
- GitHub

---

## 🔄 Fluxo da Aplicação

### 1. Carregamento dos Países

A aplicação consulta o endpoint:

```http
GET /teams/countries
```

para preencher automaticamente o dropdown de seleções.

### 2. Descoberta do ID da Seleção

Ao selecionar um país, a aplicação consulta:

```http
GET /teams?name={pais}
```

para localizar o ID da seleção.

### 3. Carregamento dos Jogadores

Utilizando o ID encontrado, a aplicação consulta:

```http
GET /players/squads?team={id}
```

e obtém a lista de jogadores da seleção.

---

## 🎯 Funcionalidades

✅ Carregamento dinâmico de países

✅ Seleção de país através de dropdown

✅ Encadeamento assíncrono de requisições

✅ Exibição das figurinhas dos jogadores

✅ Tradução dos países para português

✅ Tradução das posições para português

✅ Exibição da bandeira da seleção

✅ Interface responsiva utilizando CSS Grid

---

## 📂 Estrutura do Projeto

```text
src/
├── components/
│   └── CardJogador.vue
│
├── services/
│   └── apiFootball.js
│
├── App.vue
├── main.js
```

---

## ▶️ Como Executar

### Instalar dependências

```bash
npm install
```

### Executar em ambiente de desenvolvimento

```bash
npm run dev
```

### Gerar versão de produção

```bash
npm run build
```

---

## 👨‍💻 Autor

Miguel Ferreira

Projeto desenvolvido como atividade prática da disciplina de Desenvolvimento Web utilizando Vue 3 e consumo de APIs REST.
