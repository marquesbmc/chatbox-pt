# 🤖 Transformer Chatbox – Assistente Inteligente para Máquinas de Autoatendimento

Este projeto implementa um modelo de linguagem baseado no **PTT5-base** (T5 em português), treinado para atuar como assistente conversacional em **máquinas automáticas de venda de refrigerantes e snacks**.

O notebook [`tranformer_chatbox.ipynb`](./tranformer_chatbox.ipynb) realiza o fine-tuning de um modelo transformer com dados curados em português, simulando situações reais de atendimento automatizado.

---

## 📌 Objetivo

Desenvolver um chatbot eficiente, leve e adaptado ao contexto de **autoatendimento físico**, capaz de responder perguntas frequentes relacionadas a:

- Sabores disponíveis
- Produtos e promoções
- Pagamento e reembolso
- Falhas operacionais
- Idioma, acessibilidade e horário de funcionamento

---

## 🧠 Arquitetura do modelo

- Modelo base: [`unicamp-dl/ptt5-base-portuguese-vocab`](https://huggingface.co/unicamp-dl/ptt5-base-portuguese-vocab)
- Biblioteca: [🤗 Hugging Face Transformers](https://github.com/huggingface/transformers)
- Framework: PyTorch

---

## 🗂️ Dataset personalizado

O dataset contém **1.100 exemplos**, organizados em **11 tópicos**, com 4 categorias de variação por tópico:

| Tipo de pergunta               | Descrição |
|-------------------------------|-----------|
| ✅ Estrutura direta            | Frases comuns, variadas e objetivas |
| ✍️ Estilo/contexto            | Variações formais, informais e regionais |
| ❌ Casos de erro ou exceção   | Perguntas sobre falhas, limitações, indisponibilidades |
| 💡 Curiosidades/indiretas     | Perguntas abertas, implícitas ou de contexto |

O arquivo `dataset.csv` com todos os exemplos organizados também está incluído neste repositório.

---

## 🚀 Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/transformer-chatbox.git
   cd transformer-chatbox
   ```

2. Instale os requisitos:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o notebook:
   - Abra `tranformer_chatbox.ipynb` em Jupyter Notebook ou JupyterLab.
   - Execute célula por célula para treinar e testar o modelo.

---

## 📦 Dependências principais

- `transformers`
- `datasets`
- `pandas`
- `torch`

O arquivo `requirements.txt` com todas as dependências necessárias está incluído no repositório.

---

## ✨ Exemplos de uso

```python
responder("A máquina aceita Pix?")
# ➜ "Sim, você pode pagar com Pix, cartão ou dinheiro."
```

```python
responder("Tem refrigerante com sabor de limão?")
# ➜ "Sim, temos refrigerantes de limão e outros sabores cítricos."
```

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](./LICENSE) para mais detalhes.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir *issues*, propor melhorias ou adaptar este projeto para outros domínios de autoatendimento.

