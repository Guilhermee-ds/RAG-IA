# RAG com IA para Consulta de Leis Brasileiras

Este projeto implementa um sistema de **Retrieval-Augmented Generation (RAG)** utilizando **LangChain** e **Ollama** para permitir a consulta inteligente a documentos jurídicos. A aplicação permite ao usuário carregar um PDF e realizar perguntas sobre seu conteúdo, recebendo respostas geradas por IA com base no documento fornecido.

A interface do usuário é construída com **Streamlit**, permitindo uma experiência interativa e acessível diretamente pelo navegador.

## 🚀 Tecnologias Utilizadas

- **Python** - Linguagem principal do projeto
- **LangChain** - Framework para manipulação de modelos de IA
- **OllamaEmbeddings** - Utilizado para embeddings de texto
- **Modelo deepseek-r1:1.5b** - Para processamento e geração de respostas
- **Streamlit** - Interface web simples e eficiente
- **PyMuPDF** - Extração de texto de PDFs
- **FAISS (InMemoryVectorStore)** - Para indexação e recuperação eficiente de documentos
- **CUDA (Opcional, mas recomendado)** - Para aceleração via GPU NVIDIA

## 📜 Como Funciona

1. O usuário faz o upload de um documento em PDF.
2. O sistema processa o texto e o armazena em um índice vetorial com FAISS.
3. Quando uma pergunta é feita, o sistema busca informações relevantes no índice.
4. O modelo **deepseek-r1:1.5b** gera uma resposta baseada nas informações recuperadas.
5. A resposta é exibida na interface do Streamlit.

## ⚡ Requisitos

Para obter o melhor desempenho, recomenda-se uma **GPU NVIDIA com suporte a CUDA**. No entanto, o modelo pode rodar na CPU, embora com maior tempo de resposta.

### Dependências

Instale os pacotes necessários:

```bash
pip install langchain ollama streamlit pdfplumber faiss-cpu torch
```

Se estiver utilizando uma **GPU NVIDIA**, instale a versão correta do PyTorch com suporte a CUDA:

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

## 🎯 Como Executar

1. Clone este repositório:

```bash
git clone https://github.com/Guilhermee-ds/RAG-IA
cd RAG-IA
```

2. Execute a aplicação:

```bash
streamlit run pdf_rag.py
```

3. Acesse no navegador em **http://localhost:8501**

## 📌 Exemplo de Uso

Após iniciar o sistema:
- Faça o upload de um PDF (exemplo: **Leis do Brasil** já incluído no repositório).
- Digite uma pergunta como: **"Qual é a penalidade para furto segundo o Código Penal?"**
- O modelo buscará a resposta no documento e exibirá o resultado.




Se gostou do projeto, ⭐ no repositório ajuda bastante!

[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue?style=for-the-badge&logo=github)](https://github.com/Guilhermee-ds/RAG-IA)

