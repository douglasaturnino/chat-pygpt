Claro! Aqui está um modelo de `README.md` para o seu projeto em Python que utiliza Streamlit e LangChain para criar um chatbot que interage com documentos PDF:

---

# 🤖 Chat PyGPT – Chat com Seus Documentos (RAG)

Este é um aplicativo Streamlit que permite interagir com documentos PDF utilizando um modelo de linguagem (LLM) via **LangChain** e **Groq**. Basta fazer o upload dos seus arquivos e conversar com o conteúdo!

## ✨ Funcionalidades

- Upload de múltiplos arquivos PDF.
- Indexação e armazenamento vetorial dos documentos com **ChromaDB**.
- Fragmentação inteligente do texto usando `RecursiveCharacterTextSplitter`.
- Consulta aos documentos com recuperação aumentada por geração (RAG).
- Seleção de diferentes modelos LLM da **Groq**.
- Respostas formatadas em **Markdown** com foco em visualizações elaboradas.

---

## 🚀 Como Rodar o Projeto

### 1. Clone o Repositório

```bash
git clone https://github.com/seu-usuario/chat-pygpt.git
cd chat-pygpt
```

### 2. Crie e Ative o Ambiente Virtual

```bash
uv sync
source .venv/bin/activate  # no Windows: .venv\Scripts\activate
```

### 4. Configure as Variáveis de Ambiente

Crie um arquivo `.env` com a seguinte variável:

```env
GROQ_API_KEY=sua-chave-api-do-groq
```

> 🔐 Você pode obter uma chave de API no [site da Groq](https://console.groq.com/).

### 5. Rode o App

```bash
streamlit run app.py
```

---

## 🧠 Modelos Disponíveis

- `llama3-8b-8192`
- `llama3-70b-8192`
- `llama-3.1-8b-instant`
- `llama-3.3-70b-versatile`

Você pode selecionar o modelo desejado diretamente na **sidebar** do aplicativo.

---

## 📁 Estrutura de Diretórios

```
chat-pygpt/
│
├── app.py                  # Código principal da aplicação Streamlit
├── db/                     # Diretório persistente dos vetores (ChromaDB)
├── .env                    # Variáveis de ambiente (não versionar)
├── pyproject.toml          # Lista de dependências do projeto
└── README.md               # Este arquivo
```

---

## 🛠️ Tecnologias Utilizadas

- [Python 3.10+](https://www.python.org/)
- [Streamlit](https://streamlit.io/)
- [LangChain](https://www.langchain.com/)
- [ChromaDB](https://www.trychroma.com/)
- [Groq LLMs](https://console.groq.com/)
- [FastEmbed](https://github.com/jiwer/fastembed)

---

## 📌 Observações

- Os arquivos PDF não são salvos, apenas processados temporariamente.
- Os dados são armazenados em um diretório local (`db/`) com persistência dos vetores.

